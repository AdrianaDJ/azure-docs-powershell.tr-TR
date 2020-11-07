---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: e88f1d3ce684881d839574fe0b73f36b83e275f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765062"
---
# <span data-ttu-id="4ba84-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="4ba84-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="4ba84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ba84-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba84-103">Kapsayıcı hizmeti için yerel bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ba84-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ba84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ba84-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ba84-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ba84-105">DESCRIPTION</span></span>
<span data-ttu-id="4ba84-106">**Yeni-AzureRmContainerServiceConfig** cmdlet 'i kapsayıcı hizmeti için yerel bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ba84-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="4ba84-107">Kapsayıcı hizmeti oluşturmak için bu nesneyi New-AzureRmContainerService cmdlet 'ine sağlayın.</span><span class="sxs-lookup"><span data-stu-id="4ba84-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="4ba84-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ba84-108">EXAMPLES</span></span>

### <span data-ttu-id="4ba84-109">Örnek 1: kapsayıcı hizmeti yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="4ba84-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="4ba84-110">Bu komut bir kapsayıcı oluşturur ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4ba84-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="4ba84-111">Komut, kapsayıcı hizmeti yapılandırması için çeşitli ayarlar belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-111">The command specifies various settings for the container service configuration.</span></span>
<span data-ttu-id="4ba84-112">Komut, ardışık düzen işlecini kullanarak yapılandırma nesnesini Add-AzureRmContainerServiceAgentPoolProfile cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4ba84-113">Bu cmdlet bir aracı havuz profili ekler.</span><span class="sxs-lookup"><span data-stu-id="4ba84-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="4ba84-114">**Yeni-AzureRmContainerService** 'In *containerservice* parametresi için $Container nesneyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="4ba84-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="4ba84-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ba84-115">PARAMETERS</span></span>

### <span data-ttu-id="4ba84-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="4ba84-116">-AdminUsername</span></span>
<span data-ttu-id="4ba84-117">Linux tabanlı kapsayıcı hizmeti için kullanılacak yönetici hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="4ba84-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="4ba84-118">-AgentPoolProfile</span></span>
<span data-ttu-id="4ba84-119">Kapsayıcı hizmeti için bir aracı havuzu profili nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="4ba84-120">Add-AzureRmContainerServiceAgentPoolProfile cmdlet 'ini kullanarak profil ekleme.</span><span class="sxs-lookup"><span data-stu-id="4ba84-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="4ba84-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="4ba84-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="4ba84-122">Özel profil Orchestrator 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="4ba84-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba84-123">-DefaultProfile</span></span>
<span data-ttu-id="4ba84-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ba84-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ba84-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="4ba84-125">-Location</span></span>
<span data-ttu-id="4ba84-126">Kapsayıcı hizmetinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="4ba84-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="4ba84-127">-MasterCount</span></span>
<span data-ttu-id="4ba84-128">Oluşturulacak ana sanal makinelerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba84-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="4ba84-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="4ba84-130">Ana sanal makinenin DNS önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="4ba84-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="4ba84-131">-OrchestratorType</span></span>
<span data-ttu-id="4ba84-132">Kapsayıcı hizmeti için Orchestrator türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="4ba84-133">Bu parametre için kabul edilebilir değerler: VSEÇCOS ve Snormal.</span><span class="sxs-lookup"><span data-stu-id="4ba84-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="4ba84-134">-Serviceprincipalprofileclıtıd</span><span class="sxs-lookup"><span data-stu-id="4ba84-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="4ba84-135">Sorumlu profil istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="4ba84-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="4ba84-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="4ba84-137">Temel profil gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="4ba84-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4ba84-138">-SshPublicKey</span></span>
<span data-ttu-id="4ba84-139">Linux tabanlı kapsayıcı hizmeti için SSH ortak anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="4ba84-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4ba84-140">-Tag</span></span>
<span data-ttu-id="4ba84-141">Kapsayıcı hizmeti için Etiketler belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-141">Specifies tags for the container service.</span></span>

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

### <span data-ttu-id="4ba84-142">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="4ba84-142">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="4ba84-143">Bu yapılandırmanın kapsayıcı hizmeti sanal makinesi için tanılamayı etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-143">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="4ba84-144">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="4ba84-144">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="4ba84-145">Windows işletim sistemini kullanan bir kapsayıcı hizmeti için yönetici parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-145">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="4ba84-146">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="4ba84-146">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="4ba84-147">Windows işletim sistemini kullanan bir kapsayıcı hizmeti için yönetici kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-147">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="4ba84-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ba84-148">-Confirm</span></span>
<span data-ttu-id="4ba84-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ba84-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba84-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba84-150">-WhatIf</span></span>
<span data-ttu-id="4ba84-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ba84-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ba84-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4ba84-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba84-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba84-153">CommonParameters</span></span>
<span data-ttu-id="4ba84-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ba84-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba84-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ba84-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba84-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ba84-156">INPUTS</span></span>

## <span data-ttu-id="4ba84-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ba84-157">OUTPUTS</span></span>

## <span data-ttu-id="4ba84-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ba84-158">NOTES</span></span>

## <span data-ttu-id="4ba84-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ba84-159">RELATED LINKS</span></span>

[<span data-ttu-id="4ba84-160">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="4ba84-160">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="4ba84-161">Yeni-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4ba84-161">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)


