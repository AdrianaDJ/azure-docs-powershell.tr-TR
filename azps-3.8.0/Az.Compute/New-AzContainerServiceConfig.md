---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: a2d55c831860f5664f0f8f3dd5312368a9e5da4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096955"
---
# <span data-ttu-id="5acfb-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="5acfb-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="5acfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5acfb-102">SYNOPSIS</span></span>
<span data-ttu-id="5acfb-103">Kapsayıcı hizmeti için yerel bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5acfb-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="5acfb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5acfb-104">SYNTAX</span></span>

```
New-AzContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5acfb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5acfb-105">DESCRIPTION</span></span>
<span data-ttu-id="5acfb-106">**Yeni-AzContainerServiceConfig** cmdlet 'i kapsayıcı hizmeti için yerel bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5acfb-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="5acfb-107">Kapsayıcı hizmeti oluşturmak için bu nesneyi New-AzContainerService cmdlet 'ine sağlayın.</span><span class="sxs-lookup"><span data-stu-id="5acfb-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="5acfb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5acfb-108">EXAMPLES</span></span>

### <span data-ttu-id="5acfb-109">Örnek 1: kapsayıcı hizmeti yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="5acfb-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="5acfb-110">Bu komut bir kapsayıcı oluşturur ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5acfb-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5acfb-111">Komut, kapsayıcı hizmeti yapılandırması için çeşitli ayarlar belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="5acfb-112">Komut, ardışık düzen işlecini kullanarak yapılandırma nesnesini Add-AzContainerServiceAgentPoolProfile cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="5acfb-113">Bu cmdlet bir aracı havuz profili ekler.</span><span class="sxs-lookup"><span data-stu-id="5acfb-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="5acfb-114">**Yeni-AzContainerService** 'In *containerservice* parametresi için $Container nesneyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="5acfb-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="5acfb-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5acfb-115">PARAMETERS</span></span>

### <span data-ttu-id="5acfb-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="5acfb-116">-AdminUsername</span></span>
<span data-ttu-id="5acfb-117">Linux tabanlı kapsayıcı hizmeti için kullanılacak yönetici hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acfb-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="5acfb-118">-AgentPoolProfile</span></span>
<span data-ttu-id="5acfb-119">Kapsayıcı hizmeti için bir aracı havuzu profili nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="5acfb-120">Add-AzContainerServiceAgentPoolProfile cmdlet 'ini kullanarak profil ekleme.</span><span class="sxs-lookup"><span data-stu-id="5acfb-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acfb-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="5acfb-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="5acfb-122">Özel profil Orchestrator 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="5acfb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5acfb-123">-DefaultProfile</span></span>
<span data-ttu-id="5acfb-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5acfb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5acfb-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="5acfb-125">-Location</span></span>
<span data-ttu-id="5acfb-126">Kapsayıcı hizmetinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acfb-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="5acfb-127">-MasterCount</span></span>
<span data-ttu-id="5acfb-128">Oluşturulacak ana sanal makinelerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acfb-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="5acfb-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="5acfb-130">Ana sanal makinenin DNS önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acfb-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="5acfb-131">-OrchestratorType</span></span>
<span data-ttu-id="5acfb-132">Kapsayıcı hizmeti için Orchestrator türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="5acfb-133">Bu parametre için kabul edilebilir değerler: VSEÇCOS ve Snormal.</span><span class="sxs-lookup"><span data-stu-id="5acfb-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acfb-134">-Serviceprincipalprofileclıtıd</span><span class="sxs-lookup"><span data-stu-id="5acfb-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="5acfb-135">Sorumlu profil istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="5acfb-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="5acfb-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="5acfb-137">Temel profil gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="5acfb-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="5acfb-138">-SshPublicKey</span></span>
<span data-ttu-id="5acfb-139">Linux tabanlı kapsayıcı hizmeti için SSH ortak anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acfb-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5acfb-140">-Tag</span></span>
<span data-ttu-id="5acfb-141">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="5acfb-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5acfb-142">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="5acfb-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acfb-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="5acfb-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="5acfb-144">Bu yapılandırmanın kapsayıcı hizmeti sanal makinesi için tanılamayı etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acfb-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="5acfb-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="5acfb-146">Windows işletim sistemini kullanan bir kapsayıcı hizmeti için yönetici parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acfb-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="5acfb-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="5acfb-148">Windows işletim sistemini kullanan bir kapsayıcı hizmeti için yönetici kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5acfb-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="5acfb-149">-Confirm</span></span>
<span data-ttu-id="5acfb-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5acfb-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5acfb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5acfb-151">-WhatIf</span></span>
<span data-ttu-id="5acfb-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5acfb-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5acfb-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5acfb-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5acfb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5acfb-154">CommonParameters</span></span>
<span data-ttu-id="5acfb-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5acfb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5acfb-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5acfb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5acfb-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5acfb-157">INPUTS</span></span>

### <span data-ttu-id="5acfb-158">System. String</span><span class="sxs-lookup"><span data-stu-id="5acfb-158">System.String</span></span>

### <span data-ttu-id="5acfb-159">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5acfb-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5acfb-160">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5acfb-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5acfb-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5acfb-161">System.Int32</span></span>

### <span data-ttu-id="5acfb-162">Microsoft. Azure. Management. COMPUTE. modeller. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="5acfb-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="5acfb-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="5acfb-163">System.String[]</span></span>

### <span data-ttu-id="5acfb-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5acfb-164">System.Boolean</span></span>

## <span data-ttu-id="5acfb-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5acfb-165">OUTPUTS</span></span>

### <span data-ttu-id="5acfb-166">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="5acfb-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="5acfb-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5acfb-167">NOTES</span></span>

## <span data-ttu-id="5acfb-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5acfb-168">RELATED LINKS</span></span>

[<span data-ttu-id="5acfb-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="5acfb-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="5acfb-170">Yeni-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5acfb-170">New-AzContainerService</span></span>](./New-AzContainerService.md)