---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: bc93355520e2e1a5a1dd0529cebfc0939d503808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760992"
---
# <span data-ttu-id="57c65-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="57c65-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="57c65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57c65-102">SYNOPSIS</span></span>
<span data-ttu-id="57c65-103">Belirtilen hizmet ve hizmet topolojisi altında bir hizmet birimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="57c65-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="57c65-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57c65-104">SYNTAX</span></span>

### <span data-ttu-id="57c65-105">ByTopologyAndServiceNames (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57c65-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57c65-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="57c65-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57c65-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="57c65-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57c65-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="57c65-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57c65-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="57c65-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57c65-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="57c65-110">DESCRIPTION</span></span>
<span data-ttu-id="57c65-111">**Yeni-AzDeploymentManagerServiceUnit** cmdlet 'i hizmet topolojisinde bir hizmet altında bir hizmet oluşturur ve bu hizmet birimini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="57c65-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="57c65-112">Hizmet birimini adına, hizmet adına, hizmet topolojisine ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="57c65-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="57c65-113">Cmdlet, bir ServiceUnit nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="57c65-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="57c65-114">Bu nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerService cmdlet 'ini kullanarak değişiklikleri hizmete uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57c65-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="57c65-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57c65-115">EXAMPLES</span></span>

### <span data-ttu-id="57c65-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="57c65-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="57c65-117">Bu cmdlet, ContosoService2 merkezi olan topoloji ContosoServiceTopology 'deki hizmet altındaki ContosoResourceGroup altında, ContosoService2Storage adında yeni bir hizmet birimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="57c65-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="57c65-118">Şablon ve parametreler dosyaları, hizmet topolojisinde ContosoServiceTopology 'de başvurulan yapıt kaynak konumuna göreli yollar olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="57c65-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="57c65-119">Bu şablonda tanımlanan kaynaklar, dağıtım modu artımlı olarak ayarlanmış şekilde hedef kaynak grubu service2ResourceGroup dağıtılacak.</span><span class="sxs-lookup"><span data-stu-id="57c65-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="57c65-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="57c65-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="57c65-121">Bu cmdlet, ContosoService2 merkezi olan topoloji ContosoServiceTopology 'deki hizmet altındaki ContosoResourceGroup altında, ContosoService2Storage adında yeni bir hizmet birimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="57c65-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="57c65-122">Şablon ve parametreler başvuruları, SAS URI 'Si olarak hizmet topoloji ContosoServiceTopology1 sağlanmadığından sağlanır.</span><span class="sxs-lookup"><span data-stu-id="57c65-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="57c65-123">Bu şablonda tanımlanan kaynaklar, dağıtım modu 'nun tamamlanması için hedef kaynak grubu service2ResourceGroup dağıtılacak.</span><span class="sxs-lookup"><span data-stu-id="57c65-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="57c65-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57c65-124">PARAMETERS</span></span>

### <span data-ttu-id="57c65-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="57c65-125">-AsJob</span></span>
<span data-ttu-id="57c65-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="57c65-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57c65-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c65-127">-DefaultProfile</span></span>
<span data-ttu-id="57c65-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57c65-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57c65-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="57c65-129">-DeploymentMode</span></span>
<span data-ttu-id="57c65-130">Hizmet birimindeki kaynakları dağıtırken kullanılacak dağıtım modu.</span><span class="sxs-lookup"><span data-stu-id="57c65-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="57c65-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="57c65-131">-Location</span></span>
<span data-ttu-id="57c65-132">Hizmet birimi kaynağının konumu.</span><span class="sxs-lookup"><span data-stu-id="57c65-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="57c65-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="57c65-133">-Name</span></span>
<span data-ttu-id="57c65-134">Hizmet biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="57c65-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="57c65-135">-Parametersaralactsourcerelativepath</span><span class="sxs-lookup"><span data-stu-id="57c65-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="57c65-136">Yapıt kaynağına göre parametreler dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="57c65-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="57c65-137">ServiceTopology 'de ArtifactSource 'un başvuruda bulunmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="57c65-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="57c65-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="57c65-138">-ParametersUri</span></span>
<span data-ttu-id="57c65-139">Parametreler dosyasının SAS URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="57c65-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="57c65-140">ServiceTopology 'de Artifactsourcebaşvurulmuş olarak başvuruluyorsa, Parametersaralactsourcerelativepath kullanarak göreli yol belirtin.</span><span class="sxs-lookup"><span data-stu-id="57c65-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="57c65-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57c65-141">-ResourceGroupName</span></span>
<span data-ttu-id="57c65-142">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="57c65-142">The resource group.</span></span>

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

### <span data-ttu-id="57c65-143">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="57c65-143">-ServiceName</span></span>
<span data-ttu-id="57c65-144">Bu hizmet biriminin parçası olduğu hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="57c65-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="57c65-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="57c65-145">-ServiceObject</span></span>
<span data-ttu-id="57c65-146">Hizmet biriminin oluşturulması gereken servis nesnesi.</span><span class="sxs-lookup"><span data-stu-id="57c65-146">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="57c65-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="57c65-147">-ServiceResourceId</span></span>
<span data-ttu-id="57c65-148">Hizmet biriminin oluşturulması gereken hizmet kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="57c65-148">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="57c65-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="57c65-149">-ServiceTopologyName</span></span>
<span data-ttu-id="57c65-150">Bu hizmet birimi bu hizmet biriminin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="57c65-150">The name of the serivce topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="57c65-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="57c65-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="57c65-152">Hizmet biriminin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="57c65-152">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="57c65-153">-Servicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="57c65-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="57c65-154">Hizmet biriminin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="57c65-154">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="57c65-155">Etiketli</span><span class="sxs-lookup"><span data-stu-id="57c65-155">-Tag</span></span>
<span data-ttu-id="57c65-156">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="57c65-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="57c65-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="57c65-157">-TargetResourceGroup</span></span>
<span data-ttu-id="57c65-158">Hizmet birimi altındaki kaynakların dağıtılacağı konumu belirler.</span><span class="sxs-lookup"><span data-stu-id="57c65-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="57c65-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="57c65-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="57c65-160">Şablon dosyasının, yapıt kaynağına göre yolu.</span><span class="sxs-lookup"><span data-stu-id="57c65-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="57c65-161">ServiceTopology 'de ArtifactSource 'un başvuruda bulunmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="57c65-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="57c65-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="57c65-162">-TemplateUri</span></span>
<span data-ttu-id="57c65-163">Şablon dosyasının SAS URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="57c65-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="57c65-164">ServiceTopology 'de Artifactsourcebaşvurulmuş olarak başvuruluyorsa, TemplateArtifactSourceRelativePath kullanarak göreli yol belirtin.</span><span class="sxs-lookup"><span data-stu-id="57c65-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="57c65-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="57c65-165">-Confirm</span></span>
<span data-ttu-id="57c65-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57c65-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57c65-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57c65-167">-WhatIf</span></span>
<span data-ttu-id="57c65-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57c65-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c65-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57c65-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57c65-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c65-170">CommonParameters</span></span>
<span data-ttu-id="57c65-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57c65-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c65-172">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c65-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c65-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57c65-173">INPUTS</span></span>

### <span data-ttu-id="57c65-174">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="57c65-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="57c65-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57c65-175">OUTPUTS</span></span>

### <span data-ttu-id="57c65-176">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="57c65-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="57c65-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57c65-177">NOTES</span></span>

## <span data-ttu-id="57c65-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57c65-178">RELATED LINKS</span></span>
