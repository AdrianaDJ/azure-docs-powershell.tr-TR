---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4a66541d870d30f2de199297417d211479ecc83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594574"
---
# <span data-ttu-id="ccd79-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="ccd79-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="ccd79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccd79-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd79-103">Yönetilen uygulama tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ccd79-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccd79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccd79-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccd79-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccd79-105">DESCRIPTION</span></span>
<span data-ttu-id="ccd79-106">**Yeni-AzureRmManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ccd79-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="ccd79-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccd79-107">EXAMPLES</span></span>

### <span data-ttu-id="ccd79-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ccd79-108">Example 1</span></span>
```
PS C:\> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName "test" -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="ccd79-109">Bu komut yönetilen uygulama tanımı oluşturur</span><span class="sxs-lookup"><span data-stu-id="ccd79-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="ccd79-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccd79-110">PARAMETERS</span></span>

### <span data-ttu-id="ccd79-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ccd79-111">-ApiVersion</span></span>
<span data-ttu-id="ccd79-112">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccd79-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ccd79-113">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ccd79-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ccd79-114">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="ccd79-114">-Authorization</span></span>
<span data-ttu-id="ccd79-115">Yönetilen uygulama tanımı yetkilendirmesi.</span><span class="sxs-lookup"><span data-stu-id="ccd79-115">The managed application definition authorization.</span></span>
<span data-ttu-id="ccd79-116">Virgülle ayrılmış yetkilendirme çiftleri \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="ccd79-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="ccd79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccd79-117">-DefaultProfile</span></span>
<span data-ttu-id="ccd79-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ccd79-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccd79-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ccd79-119">-Description</span></span>
<span data-ttu-id="ccd79-120">Yönetilen uygulama tanımı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="ccd79-120">The managed application definition description.</span></span>

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

### <span data-ttu-id="ccd79-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ccd79-121">-DisplayName</span></span>
<span data-ttu-id="ccd79-122">Yönetilen uygulama tanımı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="ccd79-122">The managed application definition display name.</span></span>

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

### <span data-ttu-id="ccd79-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="ccd79-123">-Location</span></span>
<span data-ttu-id="ccd79-124">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="ccd79-124">The resource location.</span></span>

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

### <span data-ttu-id="ccd79-125">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="ccd79-125">-LockLevel</span></span>
<span data-ttu-id="ccd79-126">Yönetilen uygulama tanımı için kilit düzeyi.</span><span class="sxs-lookup"><span data-stu-id="ccd79-126">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="ccd79-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="ccd79-127">-Name</span></span>
<span data-ttu-id="ccd79-128">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="ccd79-128">The managed application definition name.</span></span>

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

### <span data-ttu-id="ccd79-129">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="ccd79-129">-PackageFileUri</span></span>
<span data-ttu-id="ccd79-130">Yönetilen uygulama tanımlama paketi dosya URI 'si.</span><span class="sxs-lookup"><span data-stu-id="ccd79-130">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="ccd79-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ccd79-131">-Pre</span></span>
<span data-ttu-id="ccd79-132">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccd79-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ccd79-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccd79-133">-ResourceGroupName</span></span>
<span data-ttu-id="ccd79-134">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ccd79-134">The resource group name.</span></span>

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

### <span data-ttu-id="ccd79-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ccd79-135">-Tag</span></span>
<span data-ttu-id="ccd79-136">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="ccd79-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ccd79-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="ccd79-137">-Confirm</span></span>
<span data-ttu-id="ccd79-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ccd79-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccd79-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccd79-139">-WhatIf</span></span>
<span data-ttu-id="ccd79-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccd79-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccd79-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ccd79-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccd79-142">-Createuıdefinition</span><span class="sxs-lookup"><span data-stu-id="ccd79-142">-CreateUiDefinition</span></span>
<span data-ttu-id="ccd79-143">Yönetilen uygulama tanımı UI tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ccd79-143">The managed application definition create ui definition.</span></span>

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

### <span data-ttu-id="ccd79-144">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="ccd79-144">-MainTemplate</span></span>
<span data-ttu-id="ccd79-145">Yönetilen uygulama tanımı ana şablonu.</span><span class="sxs-lookup"><span data-stu-id="ccd79-145">The managed application definition main template.</span></span>

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

### <span data-ttu-id="ccd79-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd79-146">CommonParameters</span></span>
<span data-ttu-id="ccd79-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccd79-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd79-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccd79-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd79-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccd79-149">INPUTS</span></span>

### <span data-ttu-id="ccd79-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ccd79-150">System.String</span></span>
<span data-ttu-id="ccd79-151">Microsoft. Azure. Commands. ResourceManager. cmdlet. Entities. Application. ApplicationLockLevel System. String [] System. Koleksiyonlar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ccd79-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="ccd79-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccd79-152">OUTPUTS</span></span>

### <span data-ttu-id="ccd79-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ccd79-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ccd79-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccd79-154">NOTES</span></span>

## <span data-ttu-id="ccd79-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccd79-155">RELATED LINKS</span></span>

