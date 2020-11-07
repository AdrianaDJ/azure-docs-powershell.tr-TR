---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: 3451a922af2b2af469b7edba1539f52cabb64eb2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939863"
---
# <span data-ttu-id="f667f-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="f667f-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="f667f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f667f-102">SYNOPSIS</span></span>
<span data-ttu-id="f667f-103">Yönetilen uygulama tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f667f-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f667f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f667f-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f667f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f667f-105">DESCRIPTION</span></span>
<span data-ttu-id="f667f-106">**Yeni-AzureRmManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f667f-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="f667f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f667f-107">EXAMPLES</span></span>

### <span data-ttu-id="f667f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f667f-108">Example 1</span></span>
```
PS> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="f667f-109">Bu komut yönetilen uygulama tanımı oluşturur</span><span class="sxs-lookup"><span data-stu-id="f667f-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="f667f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f667f-110">PARAMETERS</span></span>

### <span data-ttu-id="f667f-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="f667f-111">-ApiVersion</span></span>
<span data-ttu-id="f667f-112">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="f667f-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f667f-113">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f667f-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f667f-114">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="f667f-114">-Authorization</span></span>
<span data-ttu-id="f667f-115">Yönetilen uygulama tanımı yetkilendirmesi.</span><span class="sxs-lookup"><span data-stu-id="f667f-115">The managed application definition authorization.</span></span>
<span data-ttu-id="f667f-116">Virgülle ayrılmış yetkilendirme çiftleri \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="f667f-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f667f-117">-Createuıdefinition</span><span class="sxs-lookup"><span data-stu-id="f667f-117">-CreateUiDefinition</span></span>
<span data-ttu-id="f667f-118">Yönetilen uygulama tanımı UI tanımı oluştur</span><span class="sxs-lookup"><span data-stu-id="f667f-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="f667f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f667f-119">-DefaultProfile</span></span>
<span data-ttu-id="f667f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f667f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f667f-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="f667f-121">-Description</span></span>
<span data-ttu-id="f667f-122">Yönetilen uygulama tanımı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="f667f-122">The managed application definition description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f667f-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f667f-123">-DisplayName</span></span>
<span data-ttu-id="f667f-124">Yönetilen uygulama tanımı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="f667f-124">The managed application definition display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f667f-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="f667f-125">-Location</span></span>
<span data-ttu-id="f667f-126">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="f667f-126">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f667f-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="f667f-127">-LockLevel</span></span>
<span data-ttu-id="f667f-128">Yönetilen uygulama tanımı için kilit düzeyi.</span><span class="sxs-lookup"><span data-stu-id="f667f-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f667f-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="f667f-129">-MainTemplate</span></span>
<span data-ttu-id="f667f-130">Yönetilen uygulama tanımı ana şablonu</span><span class="sxs-lookup"><span data-stu-id="f667f-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="f667f-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="f667f-131">-Name</span></span>
<span data-ttu-id="f667f-132">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="f667f-132">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f667f-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="f667f-133">-PackageFileUri</span></span>
<span data-ttu-id="f667f-134">Yönetilen uygulama tanımlama paketi dosya URI 'si.</span><span class="sxs-lookup"><span data-stu-id="f667f-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="f667f-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="f667f-135">-Pre</span></span>
<span data-ttu-id="f667f-136">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f667f-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f667f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f667f-137">-ResourceGroupName</span></span>
<span data-ttu-id="f667f-138">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f667f-138">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f667f-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f667f-139">-Tag</span></span>
<span data-ttu-id="f667f-140">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="f667f-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f667f-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="f667f-141">-Confirm</span></span>
<span data-ttu-id="f667f-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f667f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f667f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f667f-143">-WhatIf</span></span>
<span data-ttu-id="f667f-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f667f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f667f-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f667f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f667f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f667f-146">CommonParameters</span></span>
<span data-ttu-id="f667f-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f667f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f667f-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f667f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f667f-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f667f-149">INPUTS</span></span>

### <span data-ttu-id="f667f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f667f-150">System.String</span></span>
<span data-ttu-id="f667f-151">Microsoft. Azure. Commands. ResourceManager. cmdlet. Entities. Application. ApplicationLockLevel System. String [] System. Koleksiyonlar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f667f-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="f667f-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f667f-152">OUTPUTS</span></span>

### <span data-ttu-id="f667f-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f667f-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f667f-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f667f-154">NOTES</span></span>

## <span data-ttu-id="f667f-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f667f-155">RELATED LINKS</span></span>
