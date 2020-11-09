---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321281"
---
# <span data-ttu-id="d711a-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="d711a-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="d711a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d711a-102">SYNOPSIS</span></span>
<span data-ttu-id="d711a-103">Var olan özel kaynak sağlayıcısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d711a-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="d711a-104">Bu, düzeltme eki aracılığıyla güncelleştirilebilen tek değer etiketlerdir.</span><span class="sxs-lookup"><span data-stu-id="d711a-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="d711a-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d711a-105">SYNTAX</span></span>

### <span data-ttu-id="d711a-106">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d711a-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d711a-107">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="d711a-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d711a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d711a-108">DESCRIPTION</span></span>
<span data-ttu-id="d711a-109">Var olan özel kaynak sağlayıcısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d711a-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="d711a-110">Bu, düzeltme eki aracılığıyla güncelleştirilebilen tek değer etiketlerdir.</span><span class="sxs-lookup"><span data-stu-id="d711a-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="d711a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d711a-111">EXAMPLES</span></span>

### <span data-ttu-id="d711a-112">Örnek 1: özel sağlayıcıya etiket ekleme</span><span class="sxs-lookup"><span data-stu-id="d711a-112">Example 1: Add Tags to a custom Provider</span></span>
```powershell
PS C:\> Update-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -Tag @{MyTag="MyValue"} | Format-List

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

<span data-ttu-id="d711a-113">Özel sağlayıcının etiketlerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="d711a-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="d711a-114">Örnek 2: boru ile özel sağlayıcıyı Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="d711a-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="d711a-115">Boru kullanarak özel sağlayıcıyı güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="d711a-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="d711a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d711a-116">PARAMETERS</span></span>

### <span data-ttu-id="d711a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d711a-117">-DefaultProfile</span></span>
<span data-ttu-id="d711a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d711a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d711a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d711a-119">-InputObject</span></span>
<span data-ttu-id="d711a-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d711a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d711a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d711a-121">-Name</span></span>
<span data-ttu-id="d711a-122">Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="d711a-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d711a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d711a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d711a-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d711a-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d711a-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d711a-125">-SubscriptionId</span></span>
<span data-ttu-id="d711a-126">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d711a-126">The Azure subscription ID.</span></span>
<span data-ttu-id="d711a-127">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="d711a-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d711a-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d711a-128">-Tag</span></span>
<span data-ttu-id="d711a-129">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="d711a-129">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d711a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="d711a-130">-Confirm</span></span>
<span data-ttu-id="d711a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d711a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d711a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d711a-132">-WhatIf</span></span>
<span data-ttu-id="d711a-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d711a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d711a-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d711a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d711a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d711a-135">CommonParameters</span></span>
<span data-ttu-id="d711a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d711a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d711a-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d711a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d711a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d711a-138">INPUTS</span></span>

### <span data-ttu-id="d711a-139">Microsoft. Azure. PowerShell. cmdlet. CustomProviders. model. ıcustomprovidersıdentity</span><span class="sxs-lookup"><span data-stu-id="d711a-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="d711a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d711a-140">OUTPUTS</span></span>

### <span data-ttu-id="d711a-141">Microsoft. Azure. PowerShell. cmdlet. CustomProviders. modeller. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="d711a-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="d711a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d711a-142">NOTES</span></span>

<span data-ttu-id="d711a-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d711a-143">ALIASES</span></span>

<span data-ttu-id="d711a-144">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="d711a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d711a-145">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d711a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d711a-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d711a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d711a-147">INPUTOBJECT <ICustomProvidersIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="d711a-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d711a-148">`[AssociationName <String>]`: İlişkinin adı.</span><span class="sxs-lookup"><span data-stu-id="d711a-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="d711a-149">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="d711a-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d711a-150">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d711a-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d711a-151">`[ResourceProviderName <String>]`: Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="d711a-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="d711a-152">`[Scope <String>]`: İlişkinin kapsamı.</span><span class="sxs-lookup"><span data-stu-id="d711a-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="d711a-153">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d711a-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="d711a-154">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="d711a-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="d711a-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d711a-155">RELATED LINKS</span></span>

