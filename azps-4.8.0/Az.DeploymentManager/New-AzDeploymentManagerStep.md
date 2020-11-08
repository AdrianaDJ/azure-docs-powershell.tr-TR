---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107802"
---
# <span data-ttu-id="786fe-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="786fe-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="786fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="786fe-102">SYNOPSIS</span></span>
<span data-ttu-id="786fe-103">Adım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="786fe-103">Creates a step.</span></span>

## <span data-ttu-id="786fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="786fe-104">SYNTAX</span></span>

### <span data-ttu-id="786fe-105">Bekle (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="786fe-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="786fe-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="786fe-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="786fe-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="786fe-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="786fe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="786fe-108">DESCRIPTION</span></span>
<span data-ttu-id="786fe-109">**New-AzDeploymentManagerStep** cmdlet 'i, rollouts 'de başvurulabilen bir dağıtım adımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="786fe-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="786fe-110">*Name* , *resourcegroupname* ve gerekli özellikleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="786fe-110">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="786fe-111">Döndürülen nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerStep cmdlet 'ini kullanarak değişiklikleri adıma uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="786fe-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="786fe-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="786fe-112">EXAMPLES</span></span>

### <span data-ttu-id="786fe-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="786fe-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="786fe-114">ContosoService1WaitStep adını, kaynağın konumu olarak merkezi olan ContosoResourceGroup ile bir adım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="786fe-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="786fe-115">Duration özelliği, sonraki adımı çalıştırmadan önce tüm işlemin bekleyeceği süreyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="786fe-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="786fe-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="786fe-116">PARAMETERS</span></span>

### <span data-ttu-id="786fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="786fe-117">-DefaultProfile</span></span>
<span data-ttu-id="786fe-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="786fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="786fe-119">-Süre</span><span class="sxs-lookup"><span data-stu-id="786fe-119">-Duration</span></span>
<span data-ttu-id="786fe-120">ISO 8601 biçiminde bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="786fe-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="786fe-121">Örneğin: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="786fe-121">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: Wait
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786fe-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="786fe-122">-HealthCheckProperties</span></span>
<span data-ttu-id="786fe-123">Sistem durumu denetleme özellikleri.</span><span class="sxs-lookup"><span data-stu-id="786fe-123">The health check properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSHealthCheckStepProperties
Parameter Sets: HealthCheckObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786fe-124">-Healthcheckpropertiesfıle</span><span class="sxs-lookup"><span data-stu-id="786fe-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="786fe-125">Durum denetimi özelliklerinin tanımlandığı dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="786fe-125">The path to the file where health check properties are defined.</span></span>

```yaml
Type: System.String
Parameter Sets: HealthCheckFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786fe-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="786fe-126">-Location</span></span>
<span data-ttu-id="786fe-127">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="786fe-127">The location of the resource.</span></span>

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

### <span data-ttu-id="786fe-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="786fe-128">-Name</span></span>
<span data-ttu-id="786fe-129">Adımın adı.</span><span class="sxs-lookup"><span data-stu-id="786fe-129">The name of the step.</span></span>

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

### <span data-ttu-id="786fe-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="786fe-130">-ResourceGroupName</span></span>
<span data-ttu-id="786fe-131">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="786fe-131">The resource group.</span></span>

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

### <span data-ttu-id="786fe-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="786fe-132">-Tag</span></span>
<span data-ttu-id="786fe-133">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="786fe-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="786fe-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="786fe-134">-Confirm</span></span>
<span data-ttu-id="786fe-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="786fe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="786fe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="786fe-136">-WhatIf</span></span>
<span data-ttu-id="786fe-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="786fe-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="786fe-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="786fe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="786fe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="786fe-139">CommonParameters</span></span>
<span data-ttu-id="786fe-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="786fe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="786fe-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="786fe-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="786fe-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="786fe-142">INPUTS</span></span>

### <span data-ttu-id="786fe-143">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="786fe-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="786fe-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="786fe-144">OUTPUTS</span></span>

### <span data-ttu-id="786fe-145">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="786fe-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="786fe-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="786fe-146">NOTES</span></span>

## <span data-ttu-id="786fe-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="786fe-147">RELATED LINKS</span></span>
