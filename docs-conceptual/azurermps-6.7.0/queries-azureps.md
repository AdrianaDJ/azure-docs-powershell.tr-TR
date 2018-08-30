---
title: Azure PowerShell cmdlet'lerinin çıkışını sorgulama
description: Azure’daki kaynakları sorgulama ve sonuçları biçimlendirme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: daa39ada5b4e969264b6e8596dc7b090bb196fd5
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018924"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a><span data-ttu-id="158b0-103">Azure PowerShell cmdlet'lerinin çıkışını sorgulama</span><span class="sxs-lookup"><span data-stu-id="158b0-103">Query output of Azure PowerShell cmdlets</span></span>

<span data-ttu-id="158b0-104">PowerShell’de sorgu işlemleri yerleşik cmdlet’ler kullanılarak gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="158b0-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="158b0-105">PowerShell’de cmdlet adları **_Fiil-İsim_** biçiminde olur.</span><span class="sxs-lookup"><span data-stu-id="158b0-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="158b0-106">**_Get_** fiilini kullanan cmdlet’ler sorgu cmdlet’leridir.</span><span class="sxs-lookup"><span data-stu-id="158b0-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="158b0-107">Cmdlet isimleri, cmdlet fiilleri tarafından üzerinde eylem gerçekleştirilen Azure kaynağı türleridir.</span><span class="sxs-lookup"><span data-stu-id="158b0-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="158b0-108">Basit özellikleri seçme</span><span class="sxs-lookup"><span data-stu-id="158b0-108">Select simple properties</span></span>

<span data-ttu-id="158b0-109">Azure PowerShell’de her cmdlet için tanımlı bir varsayılan biçimlendirme vardır.</span><span class="sxs-lookup"><span data-stu-id="158b0-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="158b0-110">Her kaynak türünün en yaygın özellikleri, otomatik olarak bir tablo ya da liste biçiminde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="158b0-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="158b0-111">Çıktı biçimlendirme hakkında daha fazla bilgi edinmek için bkz. [Sorgu sonuçlarını biçimlendirme](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="158b0-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="158b0-112">Hesabınızdaki VM’lerin listesini sorgulamak için `Get-AzureRmVM` cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="158b0-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="158b0-113">Varsayılan çıktı otomatik olarak bir tablo şeklinde biçimlendirilir.</span><span class="sxs-lookup"><span data-stu-id="158b0-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="158b0-114">`Select-Object` cmdlet’ini kullanarak ilginizi çeken belirli özellikleri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="158b0-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="158b0-115">Karmaşık iç içe özellikleri seçme</span><span class="sxs-lookup"><span data-stu-id="158b0-115">Select complex nested properties</span></span>

<span data-ttu-id="158b0-116">Seçmek istediğiniz özellik JSON çıktısında derin olarak iç içe yerleştirilmişse, bu iç içe özelliğin tam yolunu sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="158b0-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="158b0-117">Aşağıdaki örnekte `Get-AzureRmVM` cmdlet’inden VM Adı ve işletim sistemi türünün nasıl seçileceği gösterilir.</span><span class="sxs-lookup"><span data-stu-id="158b0-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a><span data-ttu-id="158b0-118">Where-Object cmdlet’iyle sonuçları filtreleme</span><span class="sxs-lookup"><span data-stu-id="158b0-118">Filter results with the Where-Object cmdlet</span></span>

<span data-ttu-id="158b0-119">`Where-Object` cmdlet’i, sonucu herhangi bir özellik değerine göre filtrelemenize imkan tanır.</span><span class="sxs-lookup"><span data-stu-id="158b0-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="158b0-120">Aşağıdaki örnekte, filtre yalnızca adında "RGD" metni geçen VM’leri seçer.</span><span class="sxs-lookup"><span data-stu-id="158b0-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="158b0-121">Bir sonraki örnekte sonuçlar, boyutu 'Standart_DS1_V2' olan VM’leri döndürür.</span><span class="sxs-lookup"><span data-stu-id="158b0-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```