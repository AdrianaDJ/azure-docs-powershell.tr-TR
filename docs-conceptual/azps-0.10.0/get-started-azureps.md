---
title: Azure PowerShell’i kullanmaya başlama
description: Azure PowerShell’i kullanmaya başlama
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 8958570285e3db264b3e0bb654acb7f38526354c
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407536"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="e6234-103">Azure PowerShell’i kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="e6234-103">Get started with Azure PowerShell</span></span>

<span data-ttu-id="e6234-104">Azure PowerShell, Azure kaynaklarını komut satırından yönetmek için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="e6234-104">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="e6234-105">Azure Resource Manager modelini kullanan otomatik araçlar oluşturmak istediğinizde Azure PowerShell'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="e6234-105">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="e6234-106">Tarayıcınızda [Azure Cloud Shell](/azure/cloud-shell/overview) ile kullanmayı deneyin veya yerel makinenize yükleyin.</span><span class="sxs-lookup"><span data-stu-id="e6234-106">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="e6234-107">Bu makale Azure PowerShell'i kullanmaya başlamanıza yardımcı olur ve bu ürünün ardındaki temel kavramları öğretir.</span><span class="sxs-lookup"><span data-stu-id="e6234-107">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="e6234-108">Azure Cloud Shell'i yükleme veya çalıştırma</span><span class="sxs-lookup"><span data-stu-id="e6234-108">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="e6234-109">Azure PowerShell'i kullanmaya başlamanın en kolay yolu onu Azure Cloud Shell ortamında denemektir.</span><span class="sxs-lookup"><span data-stu-id="e6234-109">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="e6234-110">Cloud Shell'i kullanmaya başlamak için bkz. [Azure Cloud Shell'de PowerShell için hızlı başlangıç](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="e6234-110">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="e6234-111">Cloud Shell PowerShell 6'yı bir Linux kapsayıcısında çalıştırır, dolayısıyla Windows'a özel işlevler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="e6234-111">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="e6234-112">Yerel makinenize Azure PowerShell'i yüklemeye hazır olduğunuzda, [Azure PowerShell modülünü yükleme](install-az-ps.md) makalesindeki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="e6234-112">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="e6234-113">Azure'da oturum açma</span><span class="sxs-lookup"><span data-stu-id="e6234-113">Sign in to Azure</span></span>

<span data-ttu-id="e6234-114">`Connect-AzAccount` cmdlet'iyle etkileşimli olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="e6234-114">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="e6234-115">Cloud Shell kullanıyorsanız bu adımı atlayın: Azure Cloud Shell oturumunuz, Cloud Shell oturumunu başlatan ortam, abonelik ve kiracı için zaten kimlik doğrulaması yapmıştır.</span><span class="sxs-lookup"><span data-stu-id="e6234-115">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="e6234-116">ABD dışındaki bir bölgedeyseniz, oturum açarken `-Environment` parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e6234-116">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="e6234-117">[Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet'ini kullanarak bölgeniz için ortamın adını alın.</span><span class="sxs-lookup"><span data-stu-id="e6234-117">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="e6234-118">Örneğin, Azure Çin 21Vianet'te oturum açmak için:</span><span class="sxs-lookup"><span data-stu-id="e6234-118">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="e6234-119">PowerShell 5.1 ortamlarında Azure hesabınızın kullanıcı adını ve parolasını sağlamak için bir oturum açma iletişim kutusu alırsınız.</span><span class="sxs-lookup"><span data-stu-id="e6234-119">In PowerShell 5.1 environments, you'll get a sign-in dialog to provide a username and password for your Azure account.</span></span> <span data-ttu-id="e6234-120">PowerShell’in her sürümünde [https://microsoft.com/devicelogin ] üzerinde kullanmak üzere bir belirteç alırsınız.</span><span class="sxs-lookup"><span data-stu-id="e6234-120">On every other version of PowerShell, you'll get a token to use on [https://microsoft.com/devicelogin].</span></span>
<span data-ttu-id="e6234-121">Tarayıcınızda bu sayfayı açıp belirteci girin, ardından Azure hesabı kimlik bilgilerinizle oturum açın ve Azure PowerShell’i yetkilendirin.</span><span class="sxs-lookup"><span data-stu-id="e6234-121">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span>

<span data-ttu-id="e6234-122">Oturum açtıktan sonra, hangi Azure aboneliğinizin etkin olduğunu gösteren bilgiler göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="e6234-122">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="e6234-123">Hesabınızda birden fazla Azure aboneliği bulunuyorsa ve farklı bir abonelik seçmek istiyorsanız, [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) ile kullanılabilir aboneliklerinizi alabilir ve abonelik kimliğiniz ile [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet’ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6234-123">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="e6234-124">Azure PowerShell’de Azure aboneliklerinizi yönetme hakkında daha fazla bilgi almak için bkz. [Birden fazla Azure aboneliği kullanma](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e6234-124">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="e6234-125">Oturum açtıktan sonra, Azure PowerShell cmdlet'lerini kullanarak aboneliğinizdeki kaynaklara erişin ve bunları yönetin.</span><span class="sxs-lookup"><span data-stu-id="e6234-125">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="e6234-126">Oturum açma işlemi ve kimlik doğrulama yöntemleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell ile oturum açma](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e6234-126">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="e6234-127">Komutları bulma</span><span class="sxs-lookup"><span data-stu-id="e6234-127">Find commands</span></span>

<span data-ttu-id="e6234-128">Azure PowerShell cmdlet'lerinde PowerShell için standart `VERB-NOUN` adlandırma kuralına uyulur.</span><span class="sxs-lookup"><span data-stu-id="e6234-128">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="e6234-129">Burada VERB (fiil) eylemi (örneğin `New`, `Get`, `Set`, `Remove`) ve NOUN (ad) da kaynak türünü (örneğin`AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`) belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6234-129">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="e6234-130">Azure PowerShell'de adlar her zaman `Az` ön ekiyle başlar.</span><span class="sxs-lookup"><span data-stu-id="e6234-130">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="e6234-131">Standart fiillerin tam listesi için bkz. [PowerShell Komutları için onaylanmış fiiller](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="e6234-131">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="e6234-132">Kullanılabilir adları, fiilleri ve Azure PowerShell modüllerini bilmek, [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet'iyle komutları bulmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e6234-132">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="e6234-133">Örneğin, `Get` fiilinin kullanıldığı VM ile ilgili tüm komutları bulmak için:</span><span class="sxs-lookup"><span data-stu-id="e6234-133">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="e6234-134">Yaygın komutları bulmanıza yardımcı olmak için, bu tabloda `Get-Command` ile kullanılacak kaynak türü, ilgili Azure PowerShell modülü ve ad ön eki listelenir:</span><span class="sxs-lookup"><span data-stu-id="e6234-134">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="e6234-135">Kaynak türü</span><span class="sxs-lookup"><span data-stu-id="e6234-135">Resource type</span></span> | <span data-ttu-id="e6234-136">Azure PowerShell modülü</span><span class="sxs-lookup"><span data-stu-id="e6234-136">Azure PowerShell module</span></span> | <span data-ttu-id="e6234-137">Ad ön eki</span><span class="sxs-lookup"><span data-stu-id="e6234-137">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="e6234-138">Kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="e6234-138">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="e6234-139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e6234-139">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="e6234-140">Sanal makineler</span><span class="sxs-lookup"><span data-stu-id="e6234-140">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="e6234-141">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e6234-141">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="e6234-142">Depolama hesapları</span><span class="sxs-lookup"><span data-stu-id="e6234-142">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="e6234-143">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e6234-143">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="e6234-144">Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="e6234-144">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="e6234-145">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6234-145">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="e6234-146">Web uygulamaları</span><span class="sxs-lookup"><span data-stu-id="e6234-146">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="e6234-147">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e6234-147">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="e6234-148">SQL veritabanları</span><span class="sxs-lookup"><span data-stu-id="e6234-148">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="e6234-149">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e6234-149">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="e6234-150">Azure PowerShell'deki modüllerin tam listesi için, GitHub'da barındırılan [Azure PowerShell modül listesine](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="e6234-150">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="e6234-151">Hızlı başlangıçlar ve öğreticiler ile Azure PowerShell'in temellerini öğrenme</span><span class="sxs-lookup"><span data-stu-id="e6234-151">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="e6234-152">Azure PowerShell'i kullanmaya başlamak için, sanal makineleri ayarlamaya ve bunların nasıl sorgulanacağını öğrenmeye yönelik ayrıntılı bir öğreticiyi deneyin.</span><span class="sxs-lookup"><span data-stu-id="e6234-152">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="e6234-153">Azure PowerShell ile sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6234-153">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="e6234-154">Ayrıca diğer popüler Azure hizmetleri için de Azure PowerShell hızlı başlangıçları vardır:</span><span class="sxs-lookup"><span data-stu-id="e6234-154">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="e6234-155">Depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6234-155">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="e6234-156">Nesneleri Azure Blob depolamanın içine/dışına aktarma</span><span class="sxs-lookup"><span data-stu-id="e6234-156">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="e6234-157">Azure Key Vault'tan gizli anahtarlar oluşturma ve bunları alma</span><span class="sxs-lookup"><span data-stu-id="e6234-157">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="e6234-158">Azure SQL veritabanı ve güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6234-158">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="e6234-159">Azure Container Instances’ta kapsayıcı çalıştırma</span><span class="sxs-lookup"><span data-stu-id="e6234-159">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="e6234-160">Sanal Makine Ölçek Kümesi (VMSS) oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6234-160">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="e6234-161">Standart yük dengeleyici oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6234-161">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="e6234-162">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="e6234-162">Next steps</span></span>

* [<span data-ttu-id="e6234-163">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="e6234-163">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="e6234-164">Azure PowerShell ile Azure aboneliklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="e6234-164">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="e6234-165">Azure PowerShell ile hizmet sorumluları oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6234-165">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="e6234-166">Topluluktan yardım alın:</span><span class="sxs-lookup"><span data-stu-id="e6234-166">Get help from the community:</span></span>
  * [<span data-ttu-id="e6234-167">MSDN'deki Azure forumu</span><span class="sxs-lookup"><span data-stu-id="e6234-167">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="e6234-168">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="e6234-168">Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
