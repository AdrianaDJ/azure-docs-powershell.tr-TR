---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: d1da0ce7f8a88a12b0714960a60d5b2aa523a0a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759317"
---
# <span data-ttu-id="f43ad-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="f43ad-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="f43ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f43ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f43ad-103">Yönetilen uygulama tanımını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="f43ad-103">Updates managed application definition</span></span>

## <span data-ttu-id="f43ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f43ad-104">SYNTAX</span></span>

### <span data-ttu-id="f43ad-105">Setbynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f43ad-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f43ad-106">Setbyıd</span><span class="sxs-lookup"><span data-stu-id="f43ad-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f43ad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f43ad-107">DESCRIPTION</span></span>
<span data-ttu-id="f43ad-108">**Set-AzManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımlarını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="f43ad-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="f43ad-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f43ad-109">EXAMPLES</span></span>

### <span data-ttu-id="f43ad-110">Örnek 1: yönetilen uygulama tanımı açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f43ad-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="f43ad-111">Bu komut, yönetilen uygulama tanımı açıklamasını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="f43ad-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="f43ad-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f43ad-112">PARAMETERS</span></span>

### <span data-ttu-id="f43ad-113">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="f43ad-113">-ApiVersion</span></span>
<span data-ttu-id="f43ad-114">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="f43ad-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f43ad-115">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f43ad-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f43ad-116">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="f43ad-116">-Authorization</span></span>
<span data-ttu-id="f43ad-117">Yönetilen uygulama tanımı yetkilendirmesi.</span><span class="sxs-lookup"><span data-stu-id="f43ad-117">The managed application definition authorization.</span></span>
<span data-ttu-id="f43ad-118">PrincipalId biçimindeki virgülle ayrılmış yetkilendirme çiftleri \< \> : \< roledefinitionıd\></span><span class="sxs-lookup"><span data-stu-id="f43ad-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="f43ad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f43ad-119">-DefaultProfile</span></span>
<span data-ttu-id="f43ad-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f43ad-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f43ad-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="f43ad-121">-Description</span></span>
<span data-ttu-id="f43ad-122">Yönetilen uygulama tanımı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="f43ad-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="f43ad-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f43ad-123">-DisplayName</span></span>
<span data-ttu-id="f43ad-124">Yönetilen uygulama tanımı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="f43ad-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="f43ad-125">-ID</span><span class="sxs-lookup"><span data-stu-id="f43ad-125">-Id</span></span>
<span data-ttu-id="f43ad-126">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="f43ad-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="f43ad-127">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname</span><span class="sxs-lookup"><span data-stu-id="f43ad-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f43ad-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="f43ad-128">-Name</span></span>
<span data-ttu-id="f43ad-129">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="f43ad-129">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f43ad-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="f43ad-130">-PackageFileUri</span></span>
<span data-ttu-id="f43ad-131">Yönetilen uygulama tanımlama paketi dosya URI 'si.</span><span class="sxs-lookup"><span data-stu-id="f43ad-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="f43ad-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="f43ad-132">-Pre</span></span>
<span data-ttu-id="f43ad-133">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f43ad-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f43ad-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f43ad-134">-ResourceGroupName</span></span>
<span data-ttu-id="f43ad-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f43ad-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f43ad-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f43ad-136">-Tag</span></span>
<span data-ttu-id="f43ad-137">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="f43ad-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="f43ad-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="f43ad-138">-Confirm</span></span>
<span data-ttu-id="f43ad-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f43ad-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f43ad-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f43ad-140">-WhatIf</span></span>
<span data-ttu-id="f43ad-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f43ad-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f43ad-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f43ad-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f43ad-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f43ad-143">CommonParameters</span></span>
<span data-ttu-id="f43ad-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f43ad-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f43ad-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f43ad-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f43ad-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f43ad-146">INPUTS</span></span>

### <span data-ttu-id="f43ad-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f43ad-147">System.String</span></span>

### <span data-ttu-id="f43ad-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="f43ad-148">System.String[]</span></span>

### <span data-ttu-id="f43ad-149">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f43ad-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f43ad-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f43ad-150">OUTPUTS</span></span>

### <span data-ttu-id="f43ad-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f43ad-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f43ad-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f43ad-152">NOTES</span></span>

## <span data-ttu-id="f43ad-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f43ad-153">RELATED LINKS</span></span>
