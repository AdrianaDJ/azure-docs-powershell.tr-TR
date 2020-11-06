---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e732463984088bbcb507eb55594f7de2114d25d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571434"
---
# <span data-ttu-id="770d3-101">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="770d3-101">New-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="770d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770d3-102">SYNOPSIS</span></span>
<span data-ttu-id="770d3-103">Hizmet topolojisinde bir hizmet altında yeni bir hizmet birimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="770d3-103">Creates a new service unit under a service in a service topology.</span></span>

## <span data-ttu-id="770d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="770d3-104">SYNTAX</span></span>

### <span data-ttu-id="770d3-105">ByTopologyAndServiceNames (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="770d3-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="770d3-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="770d3-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopology] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770d3-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="770d3-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770d3-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="770d3-108">ByServiceObject</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-Service] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770d3-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="770d3-109">ByServiceResourceId</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="770d3-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="770d3-110">DESCRIPTION</span></span>
<span data-ttu-id="770d3-111">**Yeni-AzureRmDeploymentManagerServiceUnit** cmdlet 'i hizmet topolojisinde bir hizmet altında bir hizmet oluşturur ve bu hizmet birimini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="770d3-111">The **New-AzureRmDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="770d3-112">Hizmet birimini adına, hizmet adına, hizmet topolojisine ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="770d3-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="770d3-113">Cmdlet, bir ServiceUnit nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="770d3-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="770d3-114">Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmDeploymentManagerService cmdlet 'ini kullanarak değişiklikleri hizmete uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="770d3-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="770d3-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="770d3-115">EXAMPLES</span></span>

### <span data-ttu-id="770d3-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="770d3-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="770d3-117">Bu cmdlet, ContosoService2 merkezi olan topoloji ContosoServiceTopology 'deki hizmet altındaki ContosoResourceGroup altında, ContosoService2Storage adında yeni bir hizmet birimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="770d3-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="770d3-118">Şablon ve parametreler dosyaları, hizmet topolojisinde ContosoServiceTopology 'de başvurulan yapıt kaynak konumuna göreli yollar olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="770d3-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="770d3-119">Bu şablonda tanımlanan kaynaklar, dağıtım modu artımlı olarak ayarlanmış şekilde hedef kaynak grubu service2ResourceGroup dağıtılacak.</span><span class="sxs-lookup"><span data-stu-id="770d3-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="770d3-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="770d3-120">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="770d3-121">Bu cmdlet, ContosoService2 merkezi olan topoloji ContosoServiceTopology 'deki hizmet altındaki ContosoResourceGroup altında, ContosoService2Storage adında yeni bir hizmet birimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="770d3-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="770d3-122">Şablon ve parametreler başvuruları, SAS URI 'Si olarak hizmet topoloji ContosoServiceTopology1 sağlanmadığından sağlanır.</span><span class="sxs-lookup"><span data-stu-id="770d3-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="770d3-123">Bu şablonda tanımlanan kaynaklar, dağıtım modu 'nun tamamlanması için hedef kaynak grubu service2ResourceGroup dağıtılacak.</span><span class="sxs-lookup"><span data-stu-id="770d3-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="770d3-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="770d3-124">PARAMETERS</span></span>

### <span data-ttu-id="770d3-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="770d3-125">-AsJob</span></span>
<span data-ttu-id="770d3-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="770d3-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="770d3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770d3-127">-DefaultProfile</span></span>
<span data-ttu-id="770d3-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="770d3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770d3-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="770d3-129">-DeploymentMode</span></span>
<span data-ttu-id="770d3-130">Hizmet birimindeki kaynakları dağıtırken kullanılacak dağıtım modu.</span><span class="sxs-lookup"><span data-stu-id="770d3-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770d3-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="770d3-131">-Location</span></span>
<span data-ttu-id="770d3-132">Hizmet birimi kaynağının konumu.</span><span class="sxs-lookup"><span data-stu-id="770d3-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="770d3-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="770d3-133">-Name</span></span>
<span data-ttu-id="770d3-134">Hizmet biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="770d3-134">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770d3-135">-Parametersaralactsourcerelativepath</span><span class="sxs-lookup"><span data-stu-id="770d3-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="770d3-136">Hizmet birimindeki kaynakları dağıtırken kullanılacak dağıtım modu.</span><span class="sxs-lookup"><span data-stu-id="770d3-136">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="770d3-137">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="770d3-137">-ParametersUri</span></span>
<span data-ttu-id="770d3-138">Hizmet birimindeki kaynakları dağıtırken kullanılacak dağıtım modu.</span><span class="sxs-lookup"><span data-stu-id="770d3-138">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="770d3-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770d3-139">-ResourceGroupName</span></span>
<span data-ttu-id="770d3-140">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="770d3-140">The resource group.</span></span>

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

### <span data-ttu-id="770d3-141">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="770d3-141">-Service</span></span>
<span data-ttu-id="770d3-142">Hizmet biriminin oluşturulması gereken servis nesnesi.</span><span class="sxs-lookup"><span data-stu-id="770d3-142">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770d3-143">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="770d3-143">-ServiceName</span></span>
<span data-ttu-id="770d3-144">Bu hizmet biriminin parçası olduğu hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="770d3-144">The name of the service this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770d3-145">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="770d3-145">-ServiceResourceId</span></span>
<span data-ttu-id="770d3-146">Hizmet biriminin oluşturulması gereken hizmet kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="770d3-146">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770d3-147">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="770d3-147">-ServiceTopology</span></span>
<span data-ttu-id="770d3-148">Hizmet biriminin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="770d3-148">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770d3-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="770d3-149">-ServiceTopologyName</span></span>
<span data-ttu-id="770d3-150">Bu hizmet birimi bu hizmet biriminin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="770d3-150">The name of the serivce topology this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770d3-151">-Servicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="770d3-151">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="770d3-152">Hizmet biriminin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="770d3-152">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770d3-153">Etiketli</span><span class="sxs-lookup"><span data-stu-id="770d3-153">-Tag</span></span>
<span data-ttu-id="770d3-154">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="770d3-154">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="770d3-155">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="770d3-155">-TargetResourceGroup</span></span>
<span data-ttu-id="770d3-156">Hizmet birimi altındaki kaynakların dağıtılacağı konumu belirler.</span><span class="sxs-lookup"><span data-stu-id="770d3-156">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="770d3-157">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="770d3-157">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="770d3-158">Hizmet birimindeki kaynakları dağıtırken kullanılacak dağıtım modu.</span><span class="sxs-lookup"><span data-stu-id="770d3-158">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="770d3-159">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="770d3-159">-TemplateUri</span></span>
<span data-ttu-id="770d3-160">Hizmet birimindeki kaynakları dağıtırken kullanılacak dağıtım modu.</span><span class="sxs-lookup"><span data-stu-id="770d3-160">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="770d3-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="770d3-161">-Confirm</span></span>
<span data-ttu-id="770d3-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="770d3-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770d3-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770d3-163">-WhatIf</span></span>
<span data-ttu-id="770d3-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="770d3-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="770d3-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="770d3-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770d3-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770d3-166">CommonParameters</span></span>
<span data-ttu-id="770d3-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="770d3-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770d3-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="770d3-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770d3-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="770d3-169">INPUTS</span></span>

### <span data-ttu-id="770d3-170">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="770d3-170">None</span></span>

## <span data-ttu-id="770d3-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="770d3-171">OUTPUTS</span></span>

### <span data-ttu-id="770d3-172">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="770d3-172">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="770d3-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="770d3-173">NOTES</span></span>

## <span data-ttu-id="770d3-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="770d3-174">RELATED LINKS</span></span>

[<span data-ttu-id="770d3-175">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="770d3-175">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="770d3-176">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="770d3-176">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="770d3-177">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="770d3-177">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)