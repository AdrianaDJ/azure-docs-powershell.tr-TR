---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276448"
---
# <span data-ttu-id="bbb8b-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="bbb8b-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="bbb8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbb8b-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb8b-103">Belirtilen yapılandırma deposu için bir erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="bbb8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbb8b-104">SYNTAX</span></span>

### <span data-ttu-id="bbb8b-105">Regenerategenişletilen (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bbb8b-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bbb8b-106">Regenerateviaıdentitygenişletilen</span><span class="sxs-lookup"><span data-stu-id="bbb8b-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bbb8b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbb8b-107">DESCRIPTION</span></span>
<span data-ttu-id="bbb8b-108">Belirtilen yapılandırma deposu için bir erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="bbb8b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbb8b-109">EXAMPLES</span></span>

### <span data-ttu-id="bbb8b-110">Örnek 1: uygulama yapılandırma deposundaki yeniden oluşturma anahtarı</span><span class="sxs-lookup"><span data-stu-id="bbb8b-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="bbb8b-111">Bu komut, uygulama yapılandırma deposu 'nun anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="bbb8b-112">Örnek 2: nesne tarafından uygulama yapılandırma deposunu yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="bbb8b-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="bbb8b-113">Bu komut, nesne tarafından uygulama yapılandırma deposu 'nun anahtarını yeniden üret.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="bbb8b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbb8b-114">PARAMETERS</span></span>

### <span data-ttu-id="bbb8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb8b-115">-DefaultProfile</span></span>
<span data-ttu-id="bbb8b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbb8b-117">-ID</span><span class="sxs-lookup"><span data-stu-id="bbb8b-117">-Id</span></span>
<span data-ttu-id="bbb8b-118">Yeniden üretmek için anahtarın kimliği.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-118">The id of the key to regenerate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb8b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbb8b-119">-InputObject</span></span>
<span data-ttu-id="bbb8b-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb8b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bbb8b-121">-Name</span></span>
<span data-ttu-id="bbb8b-122">Yapılandırma deposu adı.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb8b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb8b-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbb8b-124">Kapsayıcı kayıt defterinin ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-124">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb8b-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="bbb8b-125">-SubscriptionId</span></span>
<span data-ttu-id="bbb8b-126">Microsoft Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-126">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb8b-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="bbb8b-127">-Confirm</span></span>
<span data-ttu-id="bbb8b-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb8b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb8b-129">-WhatIf</span></span>
<span data-ttu-id="bbb8b-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbb8b-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb8b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb8b-132">CommonParameters</span></span>
<span data-ttu-id="bbb8b-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb8b-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb8b-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbb8b-135">INPUTS</span></span>

### <span data-ttu-id="bbb8b-136">Microsoft. Azure. PowerShell. cmdlet. AppConfiguration. modeller. ıappconfigurationıdentity</span><span class="sxs-lookup"><span data-stu-id="bbb8b-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="bbb8b-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbb8b-137">OUTPUTS</span></span>

### <span data-ttu-id="bbb8b-138">Microsoft. Azure. PowerShell. cmdlet. AppConfiguration. modeller. Api20200601. ıapıkey</span><span class="sxs-lookup"><span data-stu-id="bbb8b-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="bbb8b-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbb8b-139">NOTES</span></span>

<span data-ttu-id="bbb8b-140">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="bbb8b-140">ALIASES</span></span>

<span data-ttu-id="bbb8b-141">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="bbb8b-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bbb8b-142">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bbb8b-143">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bbb8b-144">INPUTOBJECT <IAppConfigurationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="bbb8b-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bbb8b-145">`[ConfigStoreName <String>]`: Yapılandırma deposu adı.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="bbb8b-146">`[GroupName <String>]`: Özel bağlantı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="bbb8b-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="bbb8b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bbb8b-148">`[PrivateEndpointConnectionName <String>]`: Özel uç noktası bağlantı adı</span><span class="sxs-lookup"><span data-stu-id="bbb8b-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="bbb8b-149">`[ResourceGroupName <String>]`: Kapsayıcı kayıt defterinin ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="bbb8b-150">`[SubscriptionId <String>]`: Microsoft Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bbb8b-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="bbb8b-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbb8b-151">RELATED LINKS</span></span>

