---
title: Azure PowerShell’i kullanmaya başlama
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 0c3b749cb2ac7f11dacafca76b65944f523f727d
ms.sourcegitcommit: 5bdedc77b27b66998387486761ec67ed9326f169
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2019
ms.locfileid: "67346620"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="15006-102">Azure PowerShell’i kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="15006-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="15006-103">Azure PowerShell, Azure kaynaklarını komut satırından yönetmek için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="15006-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="15006-104">Azure Resource Manager modelini kullanan otomatik araçlar oluşturmak istediğinizde Azure PowerShell'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="15006-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="15006-105">Tarayıcınızda [Azure Cloud Shell](/azure/cloud-shell/overview) ile kullanmayı deneyin veya yerel makinenize yükleyin.</span><span class="sxs-lookup"><span data-stu-id="15006-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="15006-106">Bu makale Azure PowerShell'i kullanmaya başlamanıza yardımcı olur ve bu ürünün ardındaki temel kavramları öğretir.</span><span class="sxs-lookup"><span data-stu-id="15006-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="15006-107">Azure Cloud Shell'i yükleme veya çalıştırma</span><span class="sxs-lookup"><span data-stu-id="15006-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="15006-108">Azure PowerShell'i kullanmaya başlamanın en kolay yolu onu Azure Cloud Shell ortamında denemektir.</span><span class="sxs-lookup"><span data-stu-id="15006-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="15006-109">Cloud Shell'i kullanmaya başlamak için bkz. [Azure Cloud Shell'de PowerShell için hızlı başlangıç](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="15006-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="15006-110">Cloud Shell PowerShell 6'yı bir Linux kapsayıcısında çalıştırır, dolayısıyla Windows'a özel işlevler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="15006-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="15006-111">Yerel makinenize Azure PowerShell'i yüklemeye hazır olduğunuzda, [Azure PowerShell modülünü yükleme](install-az-ps.md) makalesindeki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="15006-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="15006-112">Azure'da oturum açma</span><span class="sxs-lookup"><span data-stu-id="15006-112">Sign in to Azure</span></span>

<span data-ttu-id="15006-113">`Connect-AzAccount` cmdlet'iyle etkileşimli olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="15006-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="15006-114">Cloud Shell kullanıyorsanız bu adımı atlayın: Azure Cloud Shell oturumunuz, Cloud Shell oturumunu başlatan ortam, abonelik ve kiracı için zaten kimlik doğrulaması yapmıştır.</span><span class="sxs-lookup"><span data-stu-id="15006-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="15006-115">ABD dışındaki bir bölgedeyseniz, oturum açarken `-Environment` parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="15006-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="15006-116">[Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet'ini kullanarak bölgeniz için ortamın adını alın.</span><span class="sxs-lookup"><span data-stu-id="15006-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="15006-117">Örneğin, Azure Çin 21Vianet'te oturum açmak için:</span><span class="sxs-lookup"><span data-stu-id="15006-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="15006-118">Kullanmak için bir belirteç elde edecekleriniz https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="15006-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="15006-119">Tarayıcınızda bu sayfayı açıp belirteci girin, ardından Azure hesabı kimlik bilgilerinizle oturum açın ve Azure PowerShell’i yetkilendirin.</span><span class="sxs-lookup"><span data-stu-id="15006-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="15006-120">Oturum açtıktan sonra, hangi Azure aboneliğinizin etkin olduğunu gösteren bilgiler göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="15006-120">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="15006-121">Hesabınızda birden fazla Azure aboneliği bulunuyorsa ve farklı bir abonelik seçmek istiyorsanız, [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) ile kullanılabilir aboneliklerinizi alabilir ve abonelik kimliğiniz ile [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet’ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="15006-121">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="15006-122">Azure PowerShell’de Azure aboneliklerinizi yönetme hakkında daha fazla bilgi almak için bkz. [Birden fazla Azure aboneliği kullanma](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="15006-122">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="15006-123">Oturum açtıktan sonra, Azure PowerShell cmdlet'lerini kullanarak aboneliğinizdeki kaynaklara erişin ve bunları yönetin.</span><span class="sxs-lookup"><span data-stu-id="15006-123">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="15006-124">Oturum açma işlemi ve kimlik doğrulama yöntemleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell ile oturum açma](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="15006-124">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="15006-125">Komutları bulma</span><span class="sxs-lookup"><span data-stu-id="15006-125">Find commands</span></span>

<span data-ttu-id="15006-126">Azure PowerShell cmdlet'lerinde PowerShell için standart `VERB-NOUN` adlandırma kuralına uyulur.</span><span class="sxs-lookup"><span data-stu-id="15006-126">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="15006-127">Burada VERB (fiil) eylemi (örneğin `Create`, `Get`, `Set`, `Delete`) ve NOUN (ad) da kaynak türünü (örneğin`AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`) belirtir.</span><span class="sxs-lookup"><span data-stu-id="15006-127">The verb describes the action (examples include `Create`, `Get`, `Set`, `Delete`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="15006-128">Azure PowerShell'de adlar her zaman `Az` ön ekiyle başlar.</span><span class="sxs-lookup"><span data-stu-id="15006-128">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="15006-129">Standart fiillerin tam listesi için bkz. [PowerShell Komutları için onaylanmış fiiller](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="15006-129">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="15006-130">Kullanılabilir adları, fiilleri ve Azure PowerShell modüllerini bilmek, [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet'iyle komutları bulmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="15006-130">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="15006-131">Örneğin, `Get` fiilinin kullanıldığı VM ile ilgili tüm komutları bulmak için:</span><span class="sxs-lookup"><span data-stu-id="15006-131">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="15006-132">Yaygın komutları bulmanıza yardımcı olmak için, bu tabloda `Get-Command` ile kullanılacak kaynak türü, ilgili Azure PowerShell modülü ve ad ön eki listelenir:</span><span class="sxs-lookup"><span data-stu-id="15006-132">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="15006-133">Kaynak türü</span><span class="sxs-lookup"><span data-stu-id="15006-133">Resource type</span></span> | <span data-ttu-id="15006-134">Azure PowerShell modülü</span><span class="sxs-lookup"><span data-stu-id="15006-134">Azure PowerShell module</span></span> | <span data-ttu-id="15006-135">Ad ön eki</span><span class="sxs-lookup"><span data-stu-id="15006-135">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="15006-136">Kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="15006-136">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="15006-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15006-137">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="15006-138">Sanal makineler</span><span class="sxs-lookup"><span data-stu-id="15006-138">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="15006-139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15006-139">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="15006-140">Depolama hesapları</span><span class="sxs-lookup"><span data-stu-id="15006-140">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="15006-141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="15006-141">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="15006-142">Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="15006-142">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="15006-143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="15006-143">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="15006-144">Web uygulamaları</span><span class="sxs-lookup"><span data-stu-id="15006-144">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="15006-145">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="15006-145">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="15006-146">SQL veritabanları</span><span class="sxs-lookup"><span data-stu-id="15006-146">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="15006-147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="15006-147">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="15006-148">Azure PowerShell'deki modüllerin tam listesi için, GitHub'da barındırılan [Azure PowerShell modül listesine](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="15006-148">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="15006-149">Hızlı başlangıçlar ve öğreticiler ile Azure PowerShell'in temellerini öğrenme</span><span class="sxs-lookup"><span data-stu-id="15006-149">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="15006-150">Azure PowerShell'i kullanmaya başlamak için, sanal makineleri ayarlamaya ve bunların nasıl sorgulanacağını öğrenmeye yönelik ayrıntılı bir öğreticiyi deneyin.</span><span class="sxs-lookup"><span data-stu-id="15006-150">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="15006-151">Azure PowerShell ile sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="15006-151">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="15006-152">Ayrıca diğer popüler Azure hizmetleri için de Azure PowerShell hızlı başlangıçları vardır:</span><span class="sxs-lookup"><span data-stu-id="15006-152">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="15006-153">Depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="15006-153">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="15006-154">Nesneleri Azure Blob depolamanın içine/dışına aktarma</span><span class="sxs-lookup"><span data-stu-id="15006-154">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="15006-155">Azure Key Vault'tan gizli anahtarlar oluşturma ve bunları alma</span><span class="sxs-lookup"><span data-stu-id="15006-155">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="15006-156">Azure SQL veritabanı ve güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="15006-156">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="15006-157">Azure Container Instances’ta kapsayıcı çalıştırma</span><span class="sxs-lookup"><span data-stu-id="15006-157">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="15006-158">Sanal Makine Ölçek Kümesi (VMSS) oluşturma</span><span class="sxs-lookup"><span data-stu-id="15006-158">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="15006-159">Standart yük dengeleyici oluşturma</span><span class="sxs-lookup"><span data-stu-id="15006-159">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="15006-160">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="15006-160">Next steps</span></span>

* [<span data-ttu-id="15006-161">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="15006-161">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="15006-162">Azure PowerShell ile Azure aboneliklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="15006-162">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="15006-163">Azure PowerShell ile hizmet sorumluları oluşturma</span><span class="sxs-lookup"><span data-stu-id="15006-163">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="15006-164">Topluluktan yardım alın:</span><span class="sxs-lookup"><span data-stu-id="15006-164">Get help from the community:</span></span>
  * [<span data-ttu-id="15006-165">MSDN'deki Azure forumu</span><span class="sxs-lookup"><span data-stu-id="15006-165">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="15006-166">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="15006-166">Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
