---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4dc41f7510789664b5c453285ebea032c24f3ac7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587794"
---
# <span data-ttu-id="a085d-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="a085d-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="a085d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a085d-102">SYNOPSIS</span></span>
<span data-ttu-id="a085d-103">Yönetilen uygulama tanımını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="a085d-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a085d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a085d-104">SYNTAX</span></span>

### <span data-ttu-id="a085d-105">Yönetilen uygulama tanımı adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="a085d-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="a085d-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="a085d-106">(Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a085d-107">Yönetilen uygulama tanımı kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="a085d-107">The managed application definition Id parameter set.</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a085d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a085d-108">DESCRIPTION</span></span>
<span data-ttu-id="a085d-109">**Set-AzureRmManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımlarını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="a085d-109">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="a085d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a085d-110">EXAMPLES</span></span>

### <span data-ttu-id="a085d-111">Örnek 1: yönetilen uygulama tanımı açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a085d-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="a085d-112">Bu komut, yönetilen uygulama tanımı açıklamasını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="a085d-112">This command updates the managed application definition description</span></span>

## <span data-ttu-id="a085d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a085d-113">PARAMETERS</span></span>

### <span data-ttu-id="a085d-114">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="a085d-114">-ApiVersion</span></span>
<span data-ttu-id="a085d-115">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="a085d-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a085d-116">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a085d-116">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a085d-117">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="a085d-117">-Authorization</span></span>
<span data-ttu-id="a085d-118">Yönetilen uygulama tanımı yetkilendirmesi.</span><span class="sxs-lookup"><span data-stu-id="a085d-118">The managed application definition authorization.</span></span>
<span data-ttu-id="a085d-119">Virgülle ayrılmış yetkilendirme çiftleri \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="a085d-119">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a085d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a085d-120">-DefaultProfile</span></span>
<span data-ttu-id="a085d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a085d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a085d-122">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a085d-122">-Description</span></span>
<span data-ttu-id="a085d-123">Yönetilen uygulama tanımı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="a085d-123">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a085d-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a085d-124">-DisplayName</span></span>
<span data-ttu-id="a085d-125">Yönetilen uygulama tanımı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="a085d-125">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a085d-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="a085d-126">-Name</span></span>
<span data-ttu-id="a085d-127">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="a085d-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a085d-128">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="a085d-128">-PackageFileUri</span></span>
<span data-ttu-id="a085d-129">Yönetilen uygulama tanımlama paketi dosya URI 'si.</span><span class="sxs-lookup"><span data-stu-id="a085d-129">The managed application definition package file uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a085d-130">-Pre-</span><span class="sxs-lookup"><span data-stu-id="a085d-130">-Pre</span></span>
<span data-ttu-id="a085d-131">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a085d-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a085d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a085d-132">-ResourceGroupName</span></span>
<span data-ttu-id="a085d-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a085d-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a085d-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a085d-134">-Tag</span></span>
<span data-ttu-id="a085d-135">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="a085d-135">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a085d-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="a085d-136">-Confirm</span></span>
<span data-ttu-id="a085d-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a085d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a085d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a085d-138">-WhatIf</span></span>
<span data-ttu-id="a085d-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a085d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a085d-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a085d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a085d-141">-ID</span><span class="sxs-lookup"><span data-stu-id="a085d-141">-Id</span></span>
<span data-ttu-id="a085d-142">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="a085d-142">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="a085d-143">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="a085d-143">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a085d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a085d-144">CommonParameters</span></span>
<span data-ttu-id="a085d-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a085d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a085d-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a085d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a085d-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a085d-147">INPUTS</span></span>

### <span data-ttu-id="a085d-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a085d-148">System.String</span></span>
<span data-ttu-id="a085d-149">System. String [] System. Koleksiyonlar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a085d-149">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="a085d-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a085d-150">OUTPUTS</span></span>

### <span data-ttu-id="a085d-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a085d-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a085d-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a085d-152">NOTES</span></span>

## <span data-ttu-id="a085d-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a085d-153">RELATED LINKS</span></span>

