---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: ebabe915fd203ffd73c111b0be5a2e82e2bea3a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572633"
---
# <span data-ttu-id="06213-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="06213-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="06213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06213-102">SYNOPSIS</span></span>
<span data-ttu-id="06213-103">Yönetilen uygulama tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06213-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06213-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06213-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06213-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06213-105">DESCRIPTION</span></span>
<span data-ttu-id="06213-106">**Yeni-AzureRmManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06213-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="06213-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06213-107">EXAMPLES</span></span>

### <span data-ttu-id="06213-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="06213-108">Example 1</span></span>
```
PS> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="06213-109">Bu komut yönetilen uygulama tanımı oluşturur</span><span class="sxs-lookup"><span data-stu-id="06213-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="06213-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06213-110">PARAMETERS</span></span>

### <span data-ttu-id="06213-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="06213-111">-ApiVersion</span></span>
<span data-ttu-id="06213-112">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="06213-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="06213-113">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="06213-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="06213-114">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="06213-114">-Authorization</span></span>
<span data-ttu-id="06213-115">Yönetilen uygulama tanımı yetkilendirmesi.</span><span class="sxs-lookup"><span data-stu-id="06213-115">The managed application definition authorization.</span></span>
<span data-ttu-id="06213-116">Virgülle ayrılmış yetkilendirme çiftleri \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="06213-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06213-117">-Createuıdefinition</span><span class="sxs-lookup"><span data-stu-id="06213-117">-CreateUiDefinition</span></span>
<span data-ttu-id="06213-118">Yönetilen uygulama tanımı UI tanımı oluştur</span><span class="sxs-lookup"><span data-stu-id="06213-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="06213-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06213-119">-DefaultProfile</span></span>
<span data-ttu-id="06213-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06213-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06213-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="06213-121">-Description</span></span>
<span data-ttu-id="06213-122">Yönetilen uygulama tanımı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="06213-122">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06213-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="06213-123">-DisplayName</span></span>
<span data-ttu-id="06213-124">Yönetilen uygulama tanımı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="06213-124">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06213-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="06213-125">-Location</span></span>
<span data-ttu-id="06213-126">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="06213-126">The resource location.</span></span>

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

### <span data-ttu-id="06213-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="06213-127">-LockLevel</span></span>
<span data-ttu-id="06213-128">Yönetilen uygulama tanımı için kilit düzeyi.</span><span class="sxs-lookup"><span data-stu-id="06213-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06213-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="06213-129">-MainTemplate</span></span>
<span data-ttu-id="06213-130">Yönetilen uygulama tanımı ana şablonu</span><span class="sxs-lookup"><span data-stu-id="06213-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="06213-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="06213-131">-Name</span></span>
<span data-ttu-id="06213-132">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="06213-132">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06213-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="06213-133">-PackageFileUri</span></span>
<span data-ttu-id="06213-134">Yönetilen uygulama tanımlama paketi dosya URI 'si.</span><span class="sxs-lookup"><span data-stu-id="06213-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="06213-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="06213-135">-Pre</span></span>
<span data-ttu-id="06213-136">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06213-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="06213-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06213-137">-ResourceGroupName</span></span>
<span data-ttu-id="06213-138">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="06213-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06213-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="06213-139">-Tag</span></span>
<span data-ttu-id="06213-140">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="06213-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="06213-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="06213-141">-Confirm</span></span>
<span data-ttu-id="06213-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="06213-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06213-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06213-143">-WhatIf</span></span>
<span data-ttu-id="06213-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06213-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06213-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="06213-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06213-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06213-146">CommonParameters</span></span>
<span data-ttu-id="06213-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06213-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06213-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06213-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06213-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06213-149">INPUTS</span></span>

### <span data-ttu-id="06213-150">System. String</span><span class="sxs-lookup"><span data-stu-id="06213-150">System.String</span></span>

### <span data-ttu-id="06213-151">Microsoft. Azure. Commands. ResourceManager. cmdlet. varlık. uygulama. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="06213-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="06213-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="06213-152">System.String[]</span></span>

### <span data-ttu-id="06213-153">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="06213-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="06213-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06213-154">OUTPUTS</span></span>

### <span data-ttu-id="06213-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="06213-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="06213-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06213-156">NOTES</span></span>

## <span data-ttu-id="06213-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06213-157">RELATED LINKS</span></span>
