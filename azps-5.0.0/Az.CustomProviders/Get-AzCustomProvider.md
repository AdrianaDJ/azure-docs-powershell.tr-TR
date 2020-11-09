---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321306"
---
# <span data-ttu-id="66ec0-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="66ec0-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="66ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="66ec0-103">Özel kaynak sağlayıcısı bildirimini alır.</span><span class="sxs-lookup"><span data-stu-id="66ec0-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="66ec0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66ec0-104">SYNTAX</span></span>

### <span data-ttu-id="66ec0-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66ec0-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="66ec0-106">Al</span><span class="sxs-lookup"><span data-stu-id="66ec0-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="66ec0-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="66ec0-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="66ec0-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="66ec0-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="66ec0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="66ec0-109">DESCRIPTION</span></span>
<span data-ttu-id="66ec0-110">Özel kaynak sağlayıcısı bildirimini alır.</span><span class="sxs-lookup"><span data-stu-id="66ec0-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="66ec0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66ec0-111">EXAMPLES</span></span>

### <span data-ttu-id="66ec0-112">Örnek 1: bir abonelikteki tüm özel sağlayıcıları listeleme</span><span class="sxs-lookup"><span data-stu-id="66ec0-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="66ec0-113">Bir abonelikteki tüm özel sağlayıcıları listeler</span><span class="sxs-lookup"><span data-stu-id="66ec0-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="66ec0-114">Örnek 2: tek bir özel sağlayıcı edinin</span><span class="sxs-lookup"><span data-stu-id="66ec0-114">Example 2: Get a single custom provider</span></span>
```powershell
PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :

```

<span data-ttu-id="66ec0-115">Tek bir özel sağlayıcının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="66ec0-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="66ec0-116">Ekranda nesne ayrıntılarını göstermek için Format-List kullanın.</span><span class="sxs-lookup"><span data-stu-id="66ec0-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="66ec0-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66ec0-117">PARAMETERS</span></span>

### <span data-ttu-id="66ec0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ec0-118">-DefaultProfile</span></span>
<span data-ttu-id="66ec0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66ec0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66ec0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66ec0-120">-InputObject</span></span>
<span data-ttu-id="66ec0-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="66ec0-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec0-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="66ec0-122">-Name</span></span>
<span data-ttu-id="66ec0-123">Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="66ec0-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ec0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66ec0-124">-ResourceGroupName</span></span>
<span data-ttu-id="66ec0-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="66ec0-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ec0-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="66ec0-126">-SubscriptionId</span></span>
<span data-ttu-id="66ec0-127">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="66ec0-127">The Azure subscription ID.</span></span>
<span data-ttu-id="66ec0-128">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="66ec0-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="66ec0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ec0-129">CommonParameters</span></span>
<span data-ttu-id="66ec0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66ec0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ec0-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="66ec0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ec0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66ec0-132">INPUTS</span></span>

### <span data-ttu-id="66ec0-133">Microsoft. Azure. PowerShell. cmdlet. CustomProviders. model. ıcustomprovidersıdentity</span><span class="sxs-lookup"><span data-stu-id="66ec0-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="66ec0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66ec0-134">OUTPUTS</span></span>

### <span data-ttu-id="66ec0-135">Microsoft. Azure. PowerShell. cmdlet. CustomProviders. modeller. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="66ec0-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="66ec0-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66ec0-136">NOTES</span></span>

<span data-ttu-id="66ec0-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="66ec0-137">ALIASES</span></span>

<span data-ttu-id="66ec0-138">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="66ec0-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="66ec0-139">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="66ec0-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66ec0-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66ec0-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="66ec0-141">INPUTOBJECT <ICustomProvidersIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="66ec0-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66ec0-142">`[AssociationName <String>]`: İlişkinin adı.</span><span class="sxs-lookup"><span data-stu-id="66ec0-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="66ec0-143">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="66ec0-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66ec0-144">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="66ec0-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="66ec0-145">`[ResourceProviderName <String>]`: Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="66ec0-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="66ec0-146">`[Scope <String>]`: İlişkinin kapsamı.</span><span class="sxs-lookup"><span data-stu-id="66ec0-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="66ec0-147">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="66ec0-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="66ec0-148">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="66ec0-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="66ec0-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66ec0-149">RELATED LINKS</span></span>

