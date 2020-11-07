---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 09feb94b046ef6a41130c26ae5e7b996ecbd8771
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761000"
---
# <span data-ttu-id="262e4-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="262e4-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="262e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="262e4-102">SYNOPSIS</span></span>
<span data-ttu-id="262e4-103">Yapıt kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="262e4-103">Creates an artifact source.</span></span>

## <span data-ttu-id="262e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="262e4-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="262e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="262e4-105">DESCRIPTION</span></span>
<span data-ttu-id="262e4-106">**Yeni-AzDeploymentManagerArtifactSource** cmdlet 'i bir yapıt kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="262e4-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="262e4-107">*Name* , *resourcegroupname* ve gerekli özellikleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="262e4-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="262e4-108">Döndürülen nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerArtifactSource cmdlet 'ini kullanarak yapı kaynağına değişiklikleri uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="262e4-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="262e4-109">Cmdlet, bir ServiceUnit kaynağı için gerekli yapıların bu konumdan başvurulabilmesi için, New-AzDeloymentManagerServiceTopology cmdlet 'inde başvurulabilen bir ArtifactSource nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="262e4-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeloymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="262e4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="262e4-110">EXAMPLES</span></span>

### <span data-ttu-id="262e4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="262e4-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="262e4-112">ContosoResourceGroup 'da, kaynağın konumu olarak merkezi bıze sahip olan ContosoArtifactSource adıyla bir yapıt kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="262e4-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="262e4-113">SasUri özelliği, yapıların depolandığı depolama kapsayıcısına bir Azure depolama SAS URI 'Si sağlar.</span><span class="sxs-lookup"><span data-stu-id="262e4-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="262e4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="262e4-114">PARAMETERS</span></span>

### <span data-ttu-id="262e4-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="262e4-115">-ArtifactRoot</span></span>
<span data-ttu-id="262e4-116">Yapıların depolama kapsayıcısının altındaki isteğe bağlı dizin uzaklığı.</span><span class="sxs-lookup"><span data-stu-id="262e4-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="262e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262e4-117">-DefaultProfile</span></span>
<span data-ttu-id="262e4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="262e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="262e4-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="262e4-119">-Location</span></span>
<span data-ttu-id="262e4-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="262e4-120">The location of the resource.</span></span>

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

### <span data-ttu-id="262e4-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="262e4-121">-Name</span></span>
<span data-ttu-id="262e4-122">Yapıt kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="262e4-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="262e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="262e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="262e4-124">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="262e4-124">The resource group.</span></span>

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

### <span data-ttu-id="262e4-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="262e4-125">-SasUri</span></span>
<span data-ttu-id="262e4-126">Yapıların depolandığı Azure depolama kapsayıcısının SAS URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="262e4-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="262e4-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="262e4-127">-Tag</span></span>
<span data-ttu-id="262e4-128">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="262e4-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="262e4-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="262e4-129">-Confirm</span></span>
<span data-ttu-id="262e4-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="262e4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="262e4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="262e4-131">-WhatIf</span></span>
<span data-ttu-id="262e4-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="262e4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="262e4-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="262e4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="262e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262e4-134">CommonParameters</span></span>
<span data-ttu-id="262e4-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="262e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262e4-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="262e4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262e4-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="262e4-137">INPUTS</span></span>

### <span data-ttu-id="262e4-138">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="262e4-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="262e4-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="262e4-139">OUTPUTS</span></span>

### <span data-ttu-id="262e4-140">Microsoft. Azure. Commands. DeploymentManager. modeller. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="262e4-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="262e4-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="262e4-141">NOTES</span></span>

## <span data-ttu-id="262e4-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="262e4-142">RELATED LINKS</span></span>
