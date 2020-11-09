---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326023"
---
# <span data-ttu-id="351a7-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="351a7-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="351a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="351a7-102">SYNOPSIS</span></span>
<span data-ttu-id="351a7-103">Uygulama yapılandırma depolarını alma veya listeleme.</span><span class="sxs-lookup"><span data-stu-id="351a7-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="351a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="351a7-104">SYNTAX</span></span>

### <span data-ttu-id="351a7-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="351a7-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="351a7-106">Al</span><span class="sxs-lookup"><span data-stu-id="351a7-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="351a7-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="351a7-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="351a7-108">List1</span><span class="sxs-lookup"><span data-stu-id="351a7-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="351a7-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="351a7-109">DESCRIPTION</span></span>
<span data-ttu-id="351a7-110">Uygulama yapılandırma depolarını alma veya listeleme.</span><span class="sxs-lookup"><span data-stu-id="351a7-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="351a7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="351a7-111">EXAMPLES</span></span>

### <span data-ttu-id="351a7-112">Örnek 1: aboneliğin altındaki tüm uygulama yapılandırma depolarını listeler</span><span class="sxs-lookup"><span data-stu-id="351a7-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="351a7-113">Bu komut, bir aboneliğin altındaki tüm uygulama yapılandırma depolarını listeler.</span><span class="sxs-lookup"><span data-stu-id="351a7-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="351a7-114">Örnek 2: kaynak grubu altındaki tüm uygulama yapılandırma depolarını listeler</span><span class="sxs-lookup"><span data-stu-id="351a7-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="351a7-115">Bu komut, kaynak grubu altındaki tüm uygulama yapılandırma depolarını listeler.</span><span class="sxs-lookup"><span data-stu-id="351a7-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="351a7-116">Örnek 3: ada göre bir uygulama yapılandırma deposu alma</span><span class="sxs-lookup"><span data-stu-id="351a7-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="351a7-117">Bu komut, uygulama yapılandırma deposunu adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="351a7-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="351a7-118">Örnek 4: ardışık düzene göre uygulama yapılandırma deposunu alma</span><span class="sxs-lookup"><span data-stu-id="351a7-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="351a7-119">Bu komut, bir uygulama yapılandırma deposunu ardışık düzene göre alır.</span><span class="sxs-lookup"><span data-stu-id="351a7-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="351a7-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="351a7-120">PARAMETERS</span></span>

### <span data-ttu-id="351a7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351a7-121">-DefaultProfile</span></span>
<span data-ttu-id="351a7-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="351a7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351a7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="351a7-123">-InputObject</span></span>
<span data-ttu-id="351a7-124">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="351a7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="351a7-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="351a7-125">-Name</span></span>
<span data-ttu-id="351a7-126">Yapılandırma deposu adı.</span><span class="sxs-lookup"><span data-stu-id="351a7-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="351a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="351a7-128">Kapsayıcı kayıt defterinin ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="351a7-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351a7-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="351a7-129">-SubscriptionId</span></span>
<span data-ttu-id="351a7-130">Microsoft Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="351a7-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351a7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351a7-131">CommonParameters</span></span>
<span data-ttu-id="351a7-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="351a7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351a7-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="351a7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351a7-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="351a7-134">INPUTS</span></span>

### <span data-ttu-id="351a7-135">Microsoft. Azure. PowerShell. cmdlet. AppConfiguration. modeller. ıappconfigurationıdentity</span><span class="sxs-lookup"><span data-stu-id="351a7-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="351a7-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="351a7-136">OUTPUTS</span></span>

### <span data-ttu-id="351a7-137">Microsoft. Azure. PowerShell. cmdlet. AppConfiguration. modeller. Api20200601. Iconationstore</span><span class="sxs-lookup"><span data-stu-id="351a7-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="351a7-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="351a7-138">NOTES</span></span>

<span data-ttu-id="351a7-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="351a7-139">ALIASES</span></span>

<span data-ttu-id="351a7-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="351a7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="351a7-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="351a7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="351a7-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="351a7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="351a7-143">INPUTOBJECT <IAppConfigurationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="351a7-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="351a7-144">`[ConfigStoreName <String>]`: Yapılandırma deposu adı.</span><span class="sxs-lookup"><span data-stu-id="351a7-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="351a7-145">`[GroupName <String>]`: Özel bağlantı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="351a7-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="351a7-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="351a7-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="351a7-147">`[PrivateEndpointConnectionName <String>]`: Özel uç noktası bağlantı adı</span><span class="sxs-lookup"><span data-stu-id="351a7-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="351a7-148">`[ResourceGroupName <String>]`: Kapsayıcı kayıt defterinin ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="351a7-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="351a7-149">`[SubscriptionId <String>]`: Microsoft Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="351a7-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="351a7-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="351a7-150">RELATED LINKS</span></span>

