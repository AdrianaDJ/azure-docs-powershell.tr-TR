---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: 50708e5faebff03e63b0b6330bac66c2c409adda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752140"
---
# <span data-ttu-id="83949-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="83949-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="83949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83949-102">SYNOPSIS</span></span>
<span data-ttu-id="83949-103">Belirtilen hizmet topolojisi altında bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="83949-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="83949-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83949-104">SYNTAX</span></span>

### <span data-ttu-id="83949-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="83949-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83949-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="83949-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83949-107">Byservicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="83949-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83949-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="83949-108">DESCRIPTION</span></span>
<span data-ttu-id="83949-109">**Yeni-AzDeploymentManagerService** cmdlet 'i hizmet topolojisi altında bir hizmet oluşturur ve bu hizmeti temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="83949-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="83949-110">Hizmeti adına, hizmet topolojisine ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="83949-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="83949-111">Cmdlet bir hizmet nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="83949-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="83949-112">Bu nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerService cmdlet 'ini kullanarak değişiklikleri hizmete uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="83949-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="83949-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83949-113">EXAMPLES</span></span>

### <span data-ttu-id="83949-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="83949-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="83949-115">Hizmet topolojisi altında ad ContosoService1 içeren yeni bir hizmet oluştururken, ABD 'deki konum Merkezi</span><span class="sxs-lookup"><span data-stu-id="83949-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="83949-116">TargetLocation özelliği, hizmet ContosoService1 'in belirtilen abonelikteki Doğu US bölgesine dağıtılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="83949-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="83949-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83949-117">PARAMETERS</span></span>

### <span data-ttu-id="83949-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83949-118">-DefaultProfile</span></span>
<span data-ttu-id="83949-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83949-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83949-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="83949-120">-Location</span></span>
<span data-ttu-id="83949-121">Hizmet kaynağının konumu.</span><span class="sxs-lookup"><span data-stu-id="83949-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="83949-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="83949-122">-Name</span></span>
<span data-ttu-id="83949-123">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="83949-123">The name of the service.</span></span>

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

### <span data-ttu-id="83949-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83949-124">-ResourceGroupName</span></span>
<span data-ttu-id="83949-125">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="83949-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83949-126">-Servicetopologyıd</span><span class="sxs-lookup"><span data-stu-id="83949-126">-ServiceTopologyId</span></span>
<span data-ttu-id="83949-127">Hizmetin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="83949-127">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83949-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="83949-128">-ServiceTopologyName</span></span>
<span data-ttu-id="83949-129">Bu hizmetin ait olduğu hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="83949-129">The name of the service topology this service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83949-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="83949-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="83949-131">Hizmetin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="83949-131">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83949-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="83949-132">-Tag</span></span>
<span data-ttu-id="83949-133">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="83949-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="83949-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="83949-134">-TargetLocation</span></span>
<span data-ttu-id="83949-135">Hizmetin altındaki kaynakların dağıtılacağı konumu belirler.</span><span class="sxs-lookup"><span data-stu-id="83949-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="83949-136">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="83949-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="83949-137">Hizmetin altındaki kaynakların dağıtılacağı aboneliği belirler.</span><span class="sxs-lookup"><span data-stu-id="83949-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="83949-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="83949-138">-Confirm</span></span>
<span data-ttu-id="83949-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83949-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83949-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83949-140">-WhatIf</span></span>
<span data-ttu-id="83949-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83949-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83949-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83949-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83949-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83949-143">CommonParameters</span></span>
<span data-ttu-id="83949-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83949-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83949-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83949-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83949-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83949-146">INPUTS</span></span>

### <span data-ttu-id="83949-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="83949-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="83949-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83949-148">OUTPUTS</span></span>

### <span data-ttu-id="83949-149">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="83949-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="83949-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83949-150">NOTES</span></span>

## <span data-ttu-id="83949-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83949-151">RELATED LINKS</span></span>
