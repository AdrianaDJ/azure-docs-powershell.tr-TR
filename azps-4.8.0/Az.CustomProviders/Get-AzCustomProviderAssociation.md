---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275063"
---
# <span data-ttu-id="b6d39-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="b6d39-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="b6d39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6d39-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d39-103">Bir ilişkilendirme alın.</span><span class="sxs-lookup"><span data-stu-id="b6d39-103">Get an association.</span></span>

## <span data-ttu-id="b6d39-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6d39-104">SYNTAX</span></span>

### <span data-ttu-id="b6d39-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b6d39-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b6d39-106">Al</span><span class="sxs-lookup"><span data-stu-id="b6d39-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6d39-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="b6d39-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6d39-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6d39-108">DESCRIPTION</span></span>
<span data-ttu-id="b6d39-109">Bir ilişkilendirme alın.</span><span class="sxs-lookup"><span data-stu-id="b6d39-109">Get an association.</span></span>

## <span data-ttu-id="b6d39-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6d39-110">EXAMPLES</span></span>

### <span data-ttu-id="b6d39-111">Örnek 1: özel sağlayıcı ilişkilendirmelerini Listele</span><span class="sxs-lookup"><span data-stu-id="b6d39-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="b6d39-112">Belirli bir kapsamın tüm özel sağlayıcı ilişkilendirmelerini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="b6d39-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="b6d39-113">Örnek 2: ilişkilendirme alma</span><span class="sxs-lookup"><span data-stu-id="b6d39-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="b6d39-114">Tek bir CustomProvider ilişkilendirmesinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="b6d39-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="b6d39-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6d39-115">PARAMETERS</span></span>

### <span data-ttu-id="b6d39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d39-116">-DefaultProfile</span></span>
<span data-ttu-id="b6d39-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6d39-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6d39-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6d39-118">-InputObject</span></span>
<span data-ttu-id="b6d39-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b6d39-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b6d39-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6d39-120">-Name</span></span>
<span data-ttu-id="b6d39-121">İlişkinin adı.</span><span class="sxs-lookup"><span data-stu-id="b6d39-121">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6d39-122">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="b6d39-122">-Scope</span></span>
<span data-ttu-id="b6d39-123">İlişkilendirmenin kapsamı.</span><span class="sxs-lookup"><span data-stu-id="b6d39-123">The scope of the association.</span></span>

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

### <span data-ttu-id="b6d39-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d39-124">CommonParameters</span></span>
<span data-ttu-id="b6d39-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6d39-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d39-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b6d39-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d39-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6d39-127">INPUTS</span></span>

### <span data-ttu-id="b6d39-128">Microsoft. Azure. PowerShell. cmdlet. CustomProviders. model. ıcustomprovidersıdentity</span><span class="sxs-lookup"><span data-stu-id="b6d39-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="b6d39-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6d39-129">OUTPUTS</span></span>

### <span data-ttu-id="b6d39-130">Microsoft. Azure. PowerShell. cmdlet. CustomProviders. model. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="b6d39-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="b6d39-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6d39-131">NOTES</span></span>

<span data-ttu-id="b6d39-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b6d39-132">ALIASES</span></span>

<span data-ttu-id="b6d39-133">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="b6d39-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6d39-134">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b6d39-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6d39-135">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6d39-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6d39-136">INPUTOBJECT <ICustomProvidersIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="b6d39-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6d39-137">`[AssociationName <String>]`: İlişkinin adı.</span><span class="sxs-lookup"><span data-stu-id="b6d39-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="b6d39-138">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="b6d39-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6d39-139">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b6d39-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b6d39-140">`[ResourceProviderName <String>]`: Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="b6d39-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="b6d39-141">`[Scope <String>]`: İlişkinin kapsamı.</span><span class="sxs-lookup"><span data-stu-id="b6d39-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="b6d39-142">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b6d39-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b6d39-143">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="b6d39-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b6d39-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6d39-144">RELATED LINKS</span></span>

