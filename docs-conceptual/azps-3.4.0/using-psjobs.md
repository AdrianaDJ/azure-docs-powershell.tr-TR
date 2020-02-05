---
title: PowerShell İşlerinde Azure PowerShell cmdlet'lerini çalıştırma
description: -AsJob ve Start-Job kullanarak Azure PowerShell cmdlet'lerini paralel veya arka plan görevi olarak çalıştırmayı öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: d74d3681794398534fe2c75a0c8fc314767ffa85
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002716"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a><span data-ttu-id="4efc1-103">PowerShell İşlerinde Azure PowerShell cmdlet'lerini çalıştırma</span><span class="sxs-lookup"><span data-stu-id="4efc1-103">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>

<span data-ttu-id="4efc1-104">Azure PowerShell, Azure bulutuna bağlanmaya ve yanıtları beklemeye dayanır; dolayısıyla bu cmdlet'lerin çoğu buluttan yanıt alana kadar PowerShell oturumunuzu engeller.</span><span class="sxs-lookup"><span data-stu-id="4efc1-104">Azure PowerShell depends on connecting to an Azure cloud and waiting for responses, so most of these cmdlets block your PowerShell session until they get a response from the cloud.</span></span>
<span data-ttu-id="4efc1-105">Powershell İşleri, tek bir PowerShell oturumunun içinden cmdlet'leri arka planda çalıştırmanıza veya Azure'da aynı anda birden fazla görev gerçekleştirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4efc1-105">Powershell Jobs let you run cmdlets in the background or do multiple tasks on Azure at once, from inside a single PowerShell session.</span></span>

<span data-ttu-id="4efc1-106">Bu makalede Azure PowerShell cmdlet'lerini PowerShell İşleri olarak çalıştırma ve tamamlanıp tamamlanmadığını denetleme konusuna kısa bir genel bakış sağlanır.</span><span class="sxs-lookup"><span data-stu-id="4efc1-106">This article is a brief overview of how to run Azure PowerShell cmdlets as PowerShell Jobs and check for completion.</span></span> <span data-ttu-id="4efc1-107">Komutları Azure PowerShell'de çalıştırmak için Azure PowerShell bağlamları gerekir ve bunlar [Azure bağlamları ve oturum açma bilgileri](context-persistence.md) konusunda ayrıntılı olarak açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="4efc1-107">Running commands in Azure PowerShell requires the use of Azure PowerShell contexts, which are covered in detail in [Azure contexts and sign-in credentials](context-persistence.md).</span></span>
<span data-ttu-id="4efc1-108">PowerShell İşleri hakkında daha fazla bilgi edinmek için bkz. [PowerShell İşleri hakkında](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="4efc1-108">To learn more about PowerShell Jobs, see [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="azure-contexts-with-powershell-jobs"></a><span data-ttu-id="4efc1-109">PowerShell işleri ile Azure bağlamları</span><span class="sxs-lookup"><span data-stu-id="4efc1-109">Azure contexts with PowerShell jobs</span></span>

<span data-ttu-id="4efc1-110">PowerShell İşleri, ekli bir PowerShell oturumu olmadan ayrı işlemler olarak çalışır, dolayısıyla Azure kimlik bilgilerinizin onlarla paylaşılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4efc1-110">PowerShell Jobs are run as separate processes without an attached PowerShell session, so your Azure credentials must be shared with them.</span></span> <span data-ttu-id="4efc1-111">Kimlik bilgileri Azure bağlam nesneleri olarak şu yöntemlerden biriyle geçirilir:</span><span class="sxs-lookup"><span data-stu-id="4efc1-111">Credentials are passed as Azure context objects, using one of these methods:</span></span>

* <span data-ttu-id="4efc1-112">Otomatik bağlam kalıcılığı.</span><span class="sxs-lookup"><span data-stu-id="4efc1-112">Automatic context persistence.</span></span> <span data-ttu-id="4efc1-113">Bağlam kalıcılığı varsayılan olarak etkinleştirilir ve oturum açma bilgilerinizi birden çok oturum arasında korur.</span><span class="sxs-lookup"><span data-stu-id="4efc1-113">Context persistence is enabled by default and preserves your sign-in information across multiple sessions.</span></span> <span data-ttu-id="4efc1-114">Bağlam kalıcılığı etkinleştirildiğinde geçerli Azure bağlamı yeni işleme geçirilir:</span><span class="sxs-lookup"><span data-stu-id="4efc1-114">With context persistence enabled, the current Azure context is passed to the new process:</span></span>

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* <span data-ttu-id="4efc1-115">Azure bağlam nesnesi sağlamak için Azure PowerShell cmdlet'leriyle `-AzContext` parametresini kullanın:</span><span class="sxs-lookup"><span data-stu-id="4efc1-115">Use the `-AzContext` parameter with any Azure PowerShell cmdlets to provide an Azure context object:</span></span>

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  <span data-ttu-id="4efc1-116">Bağlam kalıcılığı devre dışı bırakılırsa `-AzContext` bağımsız değişkeni gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4efc1-116">If context persistence is disabled, the `-AzContext` argument is required.</span></span>

* <span data-ttu-id="4efc1-117">Bazı Azure PowerShell cmdlet'leri tarafından sağlanan `-AsJob` anahtarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="4efc1-117">Use the `-AsJob` switch provided by some Azure PowerShell cmdlets.</span></span> <span data-ttu-id="4efc1-118">Bu anahtar cmdlet'i otomatik olarak geçerli etkin Azure bağlamını kullanıp PowerShell İşi olarak başlatır:</span><span class="sxs-lookup"><span data-stu-id="4efc1-118">This switch automatically starts the cmdlet as a PowerShell Job, using the currently active Azure context:</span></span>

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  <span data-ttu-id="4efc1-119">Cmdlet'in `-AsJob` anahtarını destekleyip desteklemediğini görmek için başvuru belgelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="4efc1-119">To see if a cmdlet supports `-AsJob`, check its reference documentation.</span></span> <span data-ttu-id="4efc1-120">`-AsJob` anahtarı bağlam otomatik kaydetme ayarının etkinleştirilmesini gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="4efc1-120">The `-AsJob` switch doesn't require context autosave to be enabled.</span></span>

<span data-ttu-id="4efc1-121">Çalışan işin durumunu denetlemek için [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4efc1-121">You can check the status of a running job with the [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet.</span></span> <span data-ttu-id="4efc1-122">Şimdiye kadar çalışan işten çıkış almak için [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4efc1-122">To get the output from a job so far, use the [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet.</span></span>

<span data-ttu-id="4efc1-123">Azure'da bir işlemin ilerleme durumunu uzaktan denetlemek için, iş tarafından değiştirilmekte olan kaynağın türüyle ilişkilendirilmiş `Get-` cmdlet'lerini kullanın:</span><span class="sxs-lookup"><span data-stu-id="4efc1-123">To check an operation's progress remotely on Azure, use the `Get-` cmdlets associated with the type of resource being modified by the job:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a><span data-ttu-id="4efc1-124">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="4efc1-124">See Also</span></span>

* [<span data-ttu-id="4efc1-125">Azure PowerShell cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="4efc1-125">Azure PowerShell contexts</span></span>](context-persistence.md)
* [<span data-ttu-id="4efc1-126">PowerShell İşleri hakkında</span><span class="sxs-lookup"><span data-stu-id="4efc1-126">About PowerShell Jobs</span></span>](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [<span data-ttu-id="4efc1-127">Get-Job başvurusu</span><span class="sxs-lookup"><span data-stu-id="4efc1-127">Get-Job reference</span></span>](/powershell/module/microsoft.powershell.core/get-job)
* [<span data-ttu-id="4efc1-128">Receive-Job başvurusu</span><span class="sxs-lookup"><span data-stu-id="4efc1-128">Receive-Job reference</span></span>](/powershell/module/microsoft.powershell.core/receive-job)
