---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: 1c59b6aba1a839086bb923556c86e3b93b80365a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932569"
---
# <span data-ttu-id="24ae8-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="24ae8-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="24ae8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="24ae8-103">Yönetilen uygulama tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24ae8-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="24ae8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24ae8-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24ae8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24ae8-105">DESCRIPTION</span></span>
<span data-ttu-id="24ae8-106">**Yeni-AzManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24ae8-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="24ae8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24ae8-107">EXAMPLES</span></span>

### <span data-ttu-id="24ae8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="24ae8-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="24ae8-109">Bu komut yönetilen uygulama tanımı oluşturur</span><span class="sxs-lookup"><span data-stu-id="24ae8-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="24ae8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24ae8-110">PARAMETERS</span></span>

### <span data-ttu-id="24ae8-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="24ae8-111">-ApiVersion</span></span>
<span data-ttu-id="24ae8-112">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="24ae8-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="24ae8-113">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="24ae8-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="24ae8-114">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="24ae8-114">-Authorization</span></span>
<span data-ttu-id="24ae8-115">Yönetilen uygulama tanımı yetkilendirmesi.</span><span class="sxs-lookup"><span data-stu-id="24ae8-115">The managed application definition authorization.</span></span>
<span data-ttu-id="24ae8-116">PrincipalId biçimindeki virgülle ayrılmış yetkilendirme çiftleri \< \> : \< roledefinitionıd\></span><span class="sxs-lookup"><span data-stu-id="24ae8-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="24ae8-117">-Createuıdefinition</span><span class="sxs-lookup"><span data-stu-id="24ae8-117">-CreateUiDefinition</span></span>
<span data-ttu-id="24ae8-118">Yönetilen uygulama tanımı UI tanımı oluştur</span><span class="sxs-lookup"><span data-stu-id="24ae8-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="24ae8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ae8-119">-DefaultProfile</span></span>
<span data-ttu-id="24ae8-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24ae8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24ae8-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="24ae8-121">-Description</span></span>
<span data-ttu-id="24ae8-122">Yönetilen uygulama tanımı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="24ae8-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="24ae8-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="24ae8-123">-DisplayName</span></span>
<span data-ttu-id="24ae8-124">Yönetilen uygulama tanımı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="24ae8-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="24ae8-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="24ae8-125">-Location</span></span>
<span data-ttu-id="24ae8-126">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="24ae8-126">The resource location.</span></span>

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

### <span data-ttu-id="24ae8-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="24ae8-127">-LockLevel</span></span>
<span data-ttu-id="24ae8-128">Yönetilen uygulama tanımı için kilit düzeyi.</span><span class="sxs-lookup"><span data-stu-id="24ae8-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="24ae8-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="24ae8-129">-MainTemplate</span></span>
<span data-ttu-id="24ae8-130">Yönetilen uygulama tanımı ana şablonu</span><span class="sxs-lookup"><span data-stu-id="24ae8-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="24ae8-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="24ae8-131">-Name</span></span>
<span data-ttu-id="24ae8-132">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="24ae8-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="24ae8-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="24ae8-133">-PackageFileUri</span></span>
<span data-ttu-id="24ae8-134">Yönetilen uygulama tanımlama paketi dosya URI 'si.</span><span class="sxs-lookup"><span data-stu-id="24ae8-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="24ae8-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="24ae8-135">-Pre</span></span>
<span data-ttu-id="24ae8-136">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="24ae8-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="24ae8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ae8-137">-ResourceGroupName</span></span>
<span data-ttu-id="24ae8-138">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="24ae8-138">The resource group name.</span></span>

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

### <span data-ttu-id="24ae8-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="24ae8-139">-Tag</span></span>
<span data-ttu-id="24ae8-140">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="24ae8-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="24ae8-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="24ae8-141">-Confirm</span></span>
<span data-ttu-id="24ae8-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="24ae8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24ae8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24ae8-143">-WhatIf</span></span>
<span data-ttu-id="24ae8-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="24ae8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24ae8-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="24ae8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24ae8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ae8-146">CommonParameters</span></span>
<span data-ttu-id="24ae8-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24ae8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ae8-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ae8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ae8-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24ae8-149">INPUTS</span></span>

### <span data-ttu-id="24ae8-150">System. String</span><span class="sxs-lookup"><span data-stu-id="24ae8-150">System.String</span></span>

### <span data-ttu-id="24ae8-151">Microsoft. Azure. Commands. ResourceManager. cmdlet. varlık. uygulama. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="24ae8-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="24ae8-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="24ae8-152">System.String[]</span></span>

### <span data-ttu-id="24ae8-153">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="24ae8-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="24ae8-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24ae8-154">OUTPUTS</span></span>

### <span data-ttu-id="24ae8-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="24ae8-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="24ae8-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24ae8-156">NOTES</span></span>

## <span data-ttu-id="24ae8-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24ae8-157">RELATED LINKS</span></span>
