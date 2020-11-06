---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: 0568359131a91beeb175d69da51d1646bd28f88e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586801"
---
# <span data-ttu-id="7b743-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="7b743-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="7b743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b743-102">SYNOPSIS</span></span>
<span data-ttu-id="7b743-103">Kapsayıcı hizmeti için yerel bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b743-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b743-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b743-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b743-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b743-105">DESCRIPTION</span></span>
<span data-ttu-id="7b743-106">**Yeni-AzureRmContainerServiceConfig** cmdlet 'i kapsayıcı hizmeti için yerel bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b743-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="7b743-107">Kapsayıcı hizmeti oluşturmak için bu nesneyi New-AzureRmContainerService cmdlet 'ine sağlayın.</span><span class="sxs-lookup"><span data-stu-id="7b743-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="7b743-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b743-108">EXAMPLES</span></span>

### <span data-ttu-id="7b743-109">Örnek 1: kapsayıcı hizmeti yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="7b743-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="7b743-110">Bu komut bir kapsayıcı oluşturur ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7b743-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="7b743-111">Komut, kapsayıcı hizmeti yapılandırması için çeşitli ayarlar belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-111">The command specifies various settings for the container service configuration.</span></span>
<span data-ttu-id="7b743-112">Komut, ardışık düzen işlecini kullanarak yapılandırma nesnesini Add-AzureRmContainerServiceAgentPoolProfile cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="7b743-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7b743-113">Bu cmdlet bir aracı havuz profili ekler.</span><span class="sxs-lookup"><span data-stu-id="7b743-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="7b743-114">**Yeni-AzureRmContainerService** 'In *containerservice* parametresi için $Container nesneyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="7b743-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="7b743-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b743-115">PARAMETERS</span></span>

### <span data-ttu-id="7b743-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="7b743-116">-AdminUsername</span></span>
<span data-ttu-id="7b743-117">Linux tabanlı kapsayıcı hizmeti için kullanılacak yönetici hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b743-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="7b743-118">-AgentPoolProfile</span></span>
<span data-ttu-id="7b743-119">Kapsayıcı hizmeti için bir aracı havuzu profili nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="7b743-120">Add-AzureRmContainerServiceAgentPoolProfile cmdlet 'ini kullanarak profil ekleme.</span><span class="sxs-lookup"><span data-stu-id="7b743-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b743-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="7b743-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="7b743-122">Özel profil Orchestrator 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="7b743-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="7b743-123">-Location</span></span>
<span data-ttu-id="7b743-124">Kapsayıcı hizmetinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-124">Specifies the location in which to create the container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b743-125">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="7b743-125">-MasterCount</span></span>
<span data-ttu-id="7b743-126">Oluşturulacak ana sanal makinelerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-126">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b743-127">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="7b743-127">-MasterDnsPrefix</span></span>
<span data-ttu-id="7b743-128">Ana sanal makinenin DNS önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-128">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b743-129">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="7b743-129">-OrchestratorType</span></span>
<span data-ttu-id="7b743-130">Kapsayıcı hizmeti için Orchestrator türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-130">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="7b743-131">Bu parametre için kabul edilebilir değerler: VSEÇCOS ve Snormal.</span><span class="sxs-lookup"><span data-stu-id="7b743-131">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: ContainerServiceOrchestratorTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b743-132">-Serviceprincipalprofileclıtıd</span><span class="sxs-lookup"><span data-stu-id="7b743-132">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="7b743-133">Sorumlu profil istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-133">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="7b743-134">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="7b743-134">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="7b743-135">Temel profil gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-135">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="7b743-136">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="7b743-136">-SshPublicKey</span></span>
<span data-ttu-id="7b743-137">Linux tabanlı kapsayıcı hizmeti için SSH ortak anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-137">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b743-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7b743-138">-Tag</span></span>
<span data-ttu-id="7b743-139">Kapsayıcı hizmeti için Etiketler belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-139">Specifies tags for the container service.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b743-140">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="7b743-140">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="7b743-141">Bu yapılandırmanın kapsayıcı hizmeti sanal makinesi için tanılamayı etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b743-141">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b743-142">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="7b743-142">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="7b743-143">Windows işletim sistemini kullanan bir kapsayıcı hizmeti için yönetici parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-143">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b743-144">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="7b743-144">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="7b743-145">Windows işletim sistemini kullanan bir kapsayıcı hizmeti için yönetici kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b743-145">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b743-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="7b743-146">-Confirm</span></span>
<span data-ttu-id="7b743-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7b743-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b743-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b743-148">-WhatIf</span></span>
<span data-ttu-id="7b743-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b743-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b743-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7b743-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b743-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b743-151">CommonParameters</span></span>
<span data-ttu-id="7b743-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b743-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b743-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b743-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b743-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b743-154">INPUTS</span></span>

### <span data-ttu-id="7b743-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7b743-155">None</span></span>
<span data-ttu-id="7b743-156">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7b743-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b743-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b743-157">OUTPUTS</span></span>

## <span data-ttu-id="7b743-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b743-158">NOTES</span></span>

## <span data-ttu-id="7b743-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b743-159">RELATED LINKS</span></span>

[<span data-ttu-id="7b743-160">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="7b743-160">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="7b743-161">Yeni-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="7b743-161">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)


