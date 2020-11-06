---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 2a242f7a265efa2dd97f967101074615381d4cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589120"
---
# <span data-ttu-id="b844b-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="b844b-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="b844b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b844b-102">SYNOPSIS</span></span>
<span data-ttu-id="b844b-103">Yönetilen uygulamayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="b844b-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b844b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b844b-104">SYNTAX</span></span>

### <span data-ttu-id="b844b-105">Yönetilen uygulama adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="b844b-105">The managed application name parameter set.</span></span> <span data-ttu-id="b844b-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="b844b-106">(Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b844b-107">Yönetilen uygulama kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="b844b-107">The managed application Id parameter set.</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b844b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b844b-108">DESCRIPTION</span></span>
<span data-ttu-id="b844b-109">**Set-AzureRmManagedApplication** cmdlet 'i yönetilen uygulamaları güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="b844b-109">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="b844b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b844b-110">EXAMPLES</span></span>

### <span data-ttu-id="b844b-111">Örnek 1: yönetilen uygulama tanımı açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b844b-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="b844b-112">Bu komut, yönetilen uygulama açıklamasını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="b844b-112">This command updates the managed application description</span></span>

## <span data-ttu-id="b844b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b844b-113">PARAMETERS</span></span>

### <span data-ttu-id="b844b-114">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="b844b-114">-ApiVersion</span></span>
<span data-ttu-id="b844b-115">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="b844b-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b844b-116">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b844b-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b844b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b844b-117">-DefaultProfile</span></span>
<span data-ttu-id="b844b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b844b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b844b-119">-Tür</span><span class="sxs-lookup"><span data-stu-id="b844b-119">-Kind</span></span>
<span data-ttu-id="b844b-120">Yönetilen uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="b844b-120">The managed application kind.</span></span>
<span data-ttu-id="b844b-121">Market veya servicecatalog 'tan biri</span><span class="sxs-lookup"><span data-stu-id="b844b-121">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="b844b-122">-Managedapplicationdefinitionıd</span><span class="sxs-lookup"><span data-stu-id="b844b-122">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="b844b-123">Yönetilen kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b844b-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="b844b-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b844b-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="b844b-125">Yönetilen kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b844b-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="b844b-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="b844b-126">-Name</span></span>
<span data-ttu-id="b844b-127">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="b844b-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b844b-128">-Parametre</span><span class="sxs-lookup"><span data-stu-id="b844b-128">-Parameter</span></span>
<span data-ttu-id="b844b-129">Yönetilen uygulama için JSON biçimli parametrelerin dizesi.</span><span class="sxs-lookup"><span data-stu-id="b844b-129">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="b844b-130">Bu, parametre içeren bir dosya adı veya URI veya parametre olarak parametre yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="b844b-130">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="b844b-131">-Plan</span><span class="sxs-lookup"><span data-stu-id="b844b-131">-Plan</span></span>
<span data-ttu-id="b844b-132">Yönetilen uygulama planı özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="b844b-132">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b844b-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="b844b-133">-Pre</span></span>
<span data-ttu-id="b844b-134">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b844b-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b844b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b844b-135">-ResourceGroupName</span></span>
<span data-ttu-id="b844b-136">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b844b-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b844b-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b844b-137">-Tag</span></span>
<span data-ttu-id="b844b-138">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="b844b-138">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b844b-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="b844b-139">-Confirm</span></span>
<span data-ttu-id="b844b-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b844b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b844b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b844b-141">-WhatIf</span></span>
<span data-ttu-id="b844b-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b844b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b844b-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b844b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b844b-144">-ID</span><span class="sxs-lookup"><span data-stu-id="b844b-144">-Id</span></span>
<span data-ttu-id="b844b-145">Abonelik dahil, tam nitelikli yönetilen uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="b844b-145">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="b844b-146">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="b844b-146">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b844b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b844b-147">CommonParameters</span></span>
<span data-ttu-id="b844b-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b844b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b844b-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b844b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b844b-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b844b-150">INPUTS</span></span>

### <span data-ttu-id="b844b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b844b-151">System.String</span></span>
<span data-ttu-id="b844b-152">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b844b-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b844b-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b844b-153">OUTPUTS</span></span>

### <span data-ttu-id="b844b-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b844b-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b844b-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b844b-155">NOTES</span></span>

## <span data-ttu-id="b844b-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b844b-156">RELATED LINKS</span></span>

