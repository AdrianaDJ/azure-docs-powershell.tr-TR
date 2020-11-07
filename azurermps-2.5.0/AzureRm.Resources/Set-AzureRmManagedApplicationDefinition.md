---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: ba2d158257f4be0e0daac8de5dd77e906e0abedc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939046"
---
# <span data-ttu-id="268f9-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="268f9-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="268f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="268f9-102">SYNOPSIS</span></span>
<span data-ttu-id="268f9-103">Yönetilen uygulama tanımını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="268f9-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="268f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="268f9-104">SYNTAX</span></span>

### <span data-ttu-id="268f9-105">Setbynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="268f9-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="268f9-106">Setbyıd</span><span class="sxs-lookup"><span data-stu-id="268f9-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="268f9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="268f9-107">DESCRIPTION</span></span>
<span data-ttu-id="268f9-108">**Set-AzureRmManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımlarını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="268f9-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="268f9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="268f9-109">EXAMPLES</span></span>

### <span data-ttu-id="268f9-110">Örnek 1: yönetilen uygulama tanımı açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="268f9-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="268f9-111">Bu komut, yönetilen uygulama tanımı açıklamasını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="268f9-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="268f9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="268f9-112">PARAMETERS</span></span>

### <span data-ttu-id="268f9-113">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="268f9-113">-ApiVersion</span></span>
<span data-ttu-id="268f9-114">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="268f9-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="268f9-115">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="268f9-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-116">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="268f9-116">-Authorization</span></span>
<span data-ttu-id="268f9-117">Yönetilen uygulama tanımı yetkilendirmesi.</span><span class="sxs-lookup"><span data-stu-id="268f9-117">The managed application definition authorization.</span></span>
<span data-ttu-id="268f9-118">Virgülle ayrılmış yetkilendirme çiftleri \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="268f9-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268f9-119">-DefaultProfile</span></span>
<span data-ttu-id="268f9-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="268f9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="268f9-121">-Description</span></span>
<span data-ttu-id="268f9-122">Yönetilen uygulama tanımı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="268f9-122">The managed application definition description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="268f9-123">-DisplayName</span></span>
<span data-ttu-id="268f9-124">Yönetilen uygulama tanımı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="268f9-124">The managed application definition display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-125">-ID</span><span class="sxs-lookup"><span data-stu-id="268f9-125">-Id</span></span>
<span data-ttu-id="268f9-126">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="268f9-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="268f9-127">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname</span><span class="sxs-lookup"><span data-stu-id="268f9-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="268f9-128">-Name</span></span>
<span data-ttu-id="268f9-129">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="268f9-129">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="268f9-130">-PackageFileUri</span></span>
<span data-ttu-id="268f9-131">Yönetilen uygulama tanımlama paketi dosya URI 'si.</span><span class="sxs-lookup"><span data-stu-id="268f9-131">The managed application definition package file uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="268f9-132">-Pre</span></span>
<span data-ttu-id="268f9-133">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="268f9-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="268f9-134">-ResourceGroupName</span></span>
<span data-ttu-id="268f9-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="268f9-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="268f9-136">-Tag</span></span>
<span data-ttu-id="268f9-137">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="268f9-137">A hash table which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="268f9-138">-Confirm</span></span>
<span data-ttu-id="268f9-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="268f9-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="268f9-140">-WhatIf</span></span>
<span data-ttu-id="268f9-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="268f9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="268f9-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="268f9-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="268f9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268f9-143">CommonParameters</span></span>
<span data-ttu-id="268f9-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="268f9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268f9-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="268f9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268f9-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="268f9-146">INPUTS</span></span>

### <span data-ttu-id="268f9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="268f9-147">System.String</span></span>
<span data-ttu-id="268f9-148">System. String [] System. Koleksiyonlar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="268f9-148">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="268f9-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="268f9-149">OUTPUTS</span></span>

### <span data-ttu-id="268f9-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="268f9-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="268f9-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="268f9-151">NOTES</span></span>

## <span data-ttu-id="268f9-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="268f9-152">RELATED LINKS</span></span>
