---
title: Azure PowerShell’i kullanmaya başlama
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 483e74d7d047562b1c170c3767495161b9c5eb2f
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342133"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="a3130-102">Azure PowerShell’i kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="a3130-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="a3130-103">Azure PowerShell, Azure kaynaklarını komut satırından yönetmek için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a3130-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="a3130-104">Azure Resource Manager modelini kullanan otomatik araçlar oluşturmak istediğinizde Azure PowerShell'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="a3130-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="a3130-105">Tarayıcınızda [Azure Cloud Shell](/azure/cloud-shell/overview) ile kullanmayı deneyin veya yerel makinenize yükleyin.</span><span class="sxs-lookup"><span data-stu-id="a3130-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="a3130-106">Bu makale Azure PowerShell'i kullanmaya başlamanıza yardımcı olur ve bu ürünün ardındaki temel kavramları öğretir.</span><span class="sxs-lookup"><span data-stu-id="a3130-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="a3130-107">Azure Cloud Shell'i yükleme veya çalıştırma</span><span class="sxs-lookup"><span data-stu-id="a3130-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="a3130-108">Azure PowerShell'i kullanmaya başlamanın en kolay yolu onu Azure Cloud Shell ortamında denemektir.</span><span class="sxs-lookup"><span data-stu-id="a3130-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="a3130-109">Cloud Shell'i kullanmaya başlamak için bkz. [Azure Cloud Shell'de PowerShell için hızlı başlangıç](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="a3130-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="a3130-110">Cloud Shell PowerShell 6'yı bir Linux kapsayıcısında çalıştırır, dolayısıyla Windows'a özel işlevler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="a3130-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="a3130-111">Yerel makinenize Azure PowerShell'i yüklemeye hazır olduğunuzda, [Azure PowerShell modülünü yükleme](install-az-ps.md) makalesindeki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="a3130-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="a3130-112">Azure'da oturum açma</span><span class="sxs-lookup"><span data-stu-id="a3130-112">Sign in to Azure</span></span>

<span data-ttu-id="a3130-113">`Connect-AzAccount` cmdlet'iyle etkileşimli olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="a3130-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="a3130-114">Cloud Shell kullanıyorsanız bu adımı atlayın: Auzre Cloud Shell oturumunuz, Cloud Shell oturumunu başlatan ortam, abonelik ve kiracı için zaten kimlik doğrulaması yapmıştır.</span><span class="sxs-lookup"><span data-stu-id="a3130-114">Skip this step if you use Cloud Shell: Your Auzre Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="a3130-115">ABD dışındaki bir bölgedeyseniz, oturum açarken `-Environment` parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a3130-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="a3130-116">[Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet'ini kullanarak bölgeniz için ortamın adını alın.</span><span class="sxs-lookup"><span data-stu-id="a3130-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="a3130-117">Örneğin, Azure Çin 21Vianet'te oturum açmak için:</span><span class="sxs-lookup"><span data-stu-id="a3130-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="a3130-118">https://microsoft.com/devicelogin sayfasında kullanabileceğiniz bir belirteç elde edersiniz.</span><span class="sxs-lookup"><span data-stu-id="a3130-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="a3130-119">Tarayıcınızda bu sayfayı açıp belirteci girin, ardından Azure hesabı kimlik bilgilerinizle oturum açın ve Azure PowerShell’i yetkilendirin.</span><span class="sxs-lookup"><span data-stu-id="a3130-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="a3130-120">Oturum açtıktan sonra, Azure PowerShell cmdlet'lerini kullanarak aboneliğinizdeki kaynaklara erişin ve bunları yönetin.</span><span class="sxs-lookup"><span data-stu-id="a3130-120">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="a3130-121">Oturum açma işlemi ve kimlik doğrulama yöntemleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell ile oturum açma](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="a3130-121">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="a3130-122">Komutları bulma</span><span class="sxs-lookup"><span data-stu-id="a3130-122">Find commands</span></span>

<span data-ttu-id="a3130-123">Azure PowerShell cmdlet'lerinde PowerShell için standart `VERB-NOUN` adlandırma kuralına uyulur.</span><span class="sxs-lookup"><span data-stu-id="a3130-123">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="a3130-124">Burada VERB (fiil) eylemi (örneğin `Create`, `Get`, `Set`, `Delete`) ve NOUN (ad) da kaynak türünü (örneğin`AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`) belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3130-124">The verb describes the action (examples include `Create`, `Get`, `Set`, `Delete`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="a3130-125">Azure PowerShell'de adlar her zaman `Az` ön ekiyle başlar.</span><span class="sxs-lookup"><span data-stu-id="a3130-125">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="a3130-126">Standart fiillerin tam listesi için bkz. [PowerShell Komutları için onaylanmış fiiller](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="a3130-126">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="a3130-127">Kullanılabilir adları, fiilleri ve Azure PowerShell modüllerini bilmek, [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet'iyle komutları bulmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a3130-127">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="a3130-128">Örneğin, `Get` fiilinin kullanıldığı VM ile ilgili tüm komutları bulmak için:</span><span class="sxs-lookup"><span data-stu-id="a3130-128">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="a3130-129">Yaygın komutları bulmanıza yardımcı olmak için, bu tabloda `Get-Command` ile kullanılacak kaynak türü, ilgili Azure PowerShell modülü ve ad ön eki listelenir:</span><span class="sxs-lookup"><span data-stu-id="a3130-129">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="a3130-130">Kaynak türü</span><span class="sxs-lookup"><span data-stu-id="a3130-130">Resource type</span></span> | <span data-ttu-id="a3130-131">Azure PowerShell modülü</span><span class="sxs-lookup"><span data-stu-id="a3130-131">Azure PowerShell module</span></span> | <span data-ttu-id="a3130-132">Ad ön eki</span><span class="sxs-lookup"><span data-stu-id="a3130-132">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="a3130-133">Kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="a3130-133">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="a3130-134">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a3130-134">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="a3130-135">Sanal makineler</span><span class="sxs-lookup"><span data-stu-id="a3130-135">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="a3130-136">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a3130-136">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="a3130-137">Depolama hesapları</span><span class="sxs-lookup"><span data-stu-id="a3130-137">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="a3130-138">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a3130-138">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="a3130-139">Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="a3130-139">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="a3130-140">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3130-140">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="a3130-141">Web uygulamaları</span><span class="sxs-lookup"><span data-stu-id="a3130-141">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="a3130-142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a3130-142">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="a3130-143">SQL veritabanları</span><span class="sxs-lookup"><span data-stu-id="a3130-143">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="a3130-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a3130-144">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="a3130-145">Azure PowerShell'deki modüllerin tam listesi için, GitHub'da barındırılan [Azure PowerShell modül listesine](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="a3130-145">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="a3130-146">Hızlı başlangıçlar ve öğreticiler ile Azure PowerShell'in temellerini öğrenme</span><span class="sxs-lookup"><span data-stu-id="a3130-146">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="a3130-147">Azure PowerShell'i kullanmaya başlamak için, sanal makineleri ayarlamaya ve bunların nasıl sorgulanacağını öğrenmeye yönelik ayrıntılı bir öğreticiyi deneyin.</span><span class="sxs-lookup"><span data-stu-id="a3130-147">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="a3130-148">Azure PowerShell ile sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="a3130-148">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="a3130-149">Ayrıca diğer popüler Azure hizmetleri için de Azure PowerShell hızlı başlangıçları vardır:</span><span class="sxs-lookup"><span data-stu-id="a3130-149">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="a3130-150">Depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="a3130-150">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="a3130-151">Nesneleri Azure Blob depolamanın içine/dışına aktarma</span><span class="sxs-lookup"><span data-stu-id="a3130-151">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="a3130-152">Azure Key Vault'tan gizli anahtarlar oluşturma ve bunları alma</span><span class="sxs-lookup"><span data-stu-id="a3130-152">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="a3130-153">Azure SQL veritabanı ve güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="a3130-153">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="a3130-154">Azure Container Instances’ta kapsayıcı çalıştırma</span><span class="sxs-lookup"><span data-stu-id="a3130-154">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="a3130-155">Sanal Makine Ölçek Kümesi (VMSS) oluşturma</span><span class="sxs-lookup"><span data-stu-id="a3130-155">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="a3130-156">Standart yük dengeleyici oluşturma</span><span class="sxs-lookup"><span data-stu-id="a3130-156">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="a3130-157">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="a3130-157">Next steps</span></span>

* [<span data-ttu-id="a3130-158">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="a3130-158">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="a3130-159">Azure PowerShell ile Azure aboneliklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="a3130-159">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="a3130-160">Azure PowerShell ile hizmet sorumluları oluşturma</span><span class="sxs-lookup"><span data-stu-id="a3130-160">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="a3130-161">Topluluktan yardım alın:</span><span class="sxs-lookup"><span data-stu-id="a3130-161">Get help from the community:</span></span>
  * [<span data-ttu-id="a3130-162">MSDN'deki Azure forumu</span><span class="sxs-lookup"><span data-stu-id="a3130-162">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="a3130-163">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="a3130-163">Stacki Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
