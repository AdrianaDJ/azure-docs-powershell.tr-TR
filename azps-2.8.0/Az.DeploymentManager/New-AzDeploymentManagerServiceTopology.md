---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 2ffae1a1d12b503e478e18d57a31fffddd9c10a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752136"
---
# <span data-ttu-id="7e7b1-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="7e7b1-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="7e7b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e7b1-103">Hizmet topolojisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-103">Creates a service topology.</span></span>

## <span data-ttu-id="7e7b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e7b1-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e7b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e7b1-105">DESCRIPTION</span></span>
<span data-ttu-id="7e7b1-106">**Yeni-AzDeploymentManagerServiceTopology** cmdlet 'i bir hizmet topolojisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="7e7b1-107">Döndürülen ServiceTopology nesnesini yerel olarak değiştirebilir ve Set-AzDeploymentManagerServiceTopology cmdlet 'ini kullanarak topolojiye değişiklikler uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="7e7b1-108">Döndürülen nesne</span><span class="sxs-lookup"><span data-stu-id="7e7b1-108">The returned object</span></span> 

<span data-ttu-id="7e7b1-109">Döndürülen nesnede, bu hizmet topolojisinde bildirilen hizmetlerin piyasaya dağıtılacağını göstermek için bir piyasaya çıkarma alanına başvurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="7e7b1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e7b1-110">EXAMPLES</span></span>

### <span data-ttu-id="7e7b1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e7b1-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="7e7b1-112">Bu cmdlet, ContosoServiceTopology adını ve ABD Merkezi konumunu içeren ContosoResourceGroup kaynak grubunda yeni bir hizmet topolojisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="7e7b1-113">Yapıt kaynağı RESOURCEID, bu topolojideki hizmet birimi tanımlarının gerektirdiği yapıların belirtilen yapıt kaynağından okunması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="7e7b1-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7e7b1-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="7e7b1-115">Bu cmdlet, ContosoServiceTopology adını ve ABD Merkezi konumunu içeren ContosoResourceGroup kaynak grubunda yeni bir hizmet topolojisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="7e7b1-116">Yapıt kaynak başvurusunun yokluğu, bu topolojideki hizmet birimi tanımları için gereken yapıların hizmet biriminde mutlak SAS URI olarak sağlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="7e7b1-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e7b1-117">PARAMETERS</span></span>

### <span data-ttu-id="7e7b1-118">-Artifactsource</span><span class="sxs-lookup"><span data-stu-id="7e7b1-118">-ArtifactSourceId</span></span>
<span data-ttu-id="7e7b1-119">Topoloji oluşturan yapıların depolandığı yapıt kaynağının tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="7e7b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e7b1-120">-DefaultProfile</span></span>
<span data-ttu-id="7e7b1-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e7b1-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="7e7b1-122">-Location</span></span>
<span data-ttu-id="7e7b1-123">Topolojinin konumu.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-123">The location of the topology.</span></span>

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

### <span data-ttu-id="7e7b1-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e7b1-124">-Name</span></span>
<span data-ttu-id="7e7b1-125">Topolojinin adı.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-125">The name of the topology.</span></span>

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

### <span data-ttu-id="7e7b1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e7b1-126">-ResourceGroupName</span></span>
<span data-ttu-id="7e7b1-127">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-127">The resource group.</span></span>

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

### <span data-ttu-id="7e7b1-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7e7b1-128">-Tag</span></span>
<span data-ttu-id="7e7b1-129">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="7e7b1-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e7b1-130">-Confirm</span></span>
<span data-ttu-id="7e7b1-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e7b1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e7b1-132">-WhatIf</span></span>
<span data-ttu-id="7e7b1-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e7b1-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e7b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e7b1-135">CommonParameters</span></span>
<span data-ttu-id="7e7b1-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e7b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e7b1-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e7b1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e7b1-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e7b1-138">INPUTS</span></span>

### <span data-ttu-id="7e7b1-139">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e7b1-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7e7b1-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e7b1-140">OUTPUTS</span></span>

### <span data-ttu-id="7e7b1-141">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="7e7b1-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="7e7b1-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e7b1-142">NOTES</span></span>

## <span data-ttu-id="7e7b1-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e7b1-143">RELATED LINKS</span></span>
