---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerserviceconfig
schema: 2.0.0
ms.openlocfilehash: 4a6f30d1f958094267b4ba8ddf09eb2e342ee889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939952"
---
# <span data-ttu-id="757a1-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="757a1-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="757a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="757a1-102">SYNOPSIS</span></span>
<span data-ttu-id="757a1-103">Kapsayıcı hizmeti için yerel bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="757a1-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="757a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="757a1-104">SYNTAX</span></span>

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

## <span data-ttu-id="757a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="757a1-105">DESCRIPTION</span></span>
<span data-ttu-id="757a1-106">**Yeni-AzureRmContainerServiceConfig** cmdlet 'i kapsayıcı hizmeti için yerel bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="757a1-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="757a1-107">Kapsayıcı hizmeti oluşturmak için bu nesneyi New-AzureRmContainerService cmdlet 'ine sağlayın.</span><span class="sxs-lookup"><span data-stu-id="757a1-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="757a1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="757a1-108">EXAMPLES</span></span>

### <span data-ttu-id="757a1-109">Örnek 1: kapsayıcı hizmeti yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="757a1-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="757a1-110">Bu komut bir kapsayıcı oluşturur ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="757a1-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="757a1-111">Komut, kapsayıcı hizmeti yapılandırması için çeşitli ayarlar belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="757a1-112">Komut, ardışık düzen işlecini kullanarak yapılandırma nesnesini Add-AzureRmContainerServiceAgentPoolProfile cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="757a1-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="757a1-113">Bu cmdlet bir aracı havuz profili ekler.</span><span class="sxs-lookup"><span data-stu-id="757a1-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="757a1-114">**Yeni-AzureRmContainerService** 'In *containerservice* parametresi için $Container nesneyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="757a1-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="757a1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="757a1-115">PARAMETERS</span></span>

### <span data-ttu-id="757a1-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="757a1-116">-AdminUsername</span></span>
<span data-ttu-id="757a1-117">Linux tabanlı kapsayıcı hizmeti için kullanılacak yönetici hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="757a1-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="757a1-118">-AgentPoolProfile</span></span>
<span data-ttu-id="757a1-119">Kapsayıcı hizmeti için bir aracı havuzu profili nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="757a1-120">Add-AzureRmContainerServiceAgentPoolProfile cmdlet 'ini kullanarak profil ekleme.</span><span class="sxs-lookup"><span data-stu-id="757a1-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="757a1-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="757a1-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="757a1-122">Özel profil Orchestrator 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="757a1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757a1-123">-DefaultProfile</span></span>
<span data-ttu-id="757a1-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="757a1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="757a1-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="757a1-125">-Location</span></span>
<span data-ttu-id="757a1-126">Kapsayıcı hizmetinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="757a1-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="757a1-127">-MasterCount</span></span>
<span data-ttu-id="757a1-128">Oluşturulacak ana sanal makinelerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="757a1-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="757a1-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="757a1-130">Ana sanal makinenin DNS önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="757a1-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="757a1-131">-OrchestratorType</span></span>
<span data-ttu-id="757a1-132">Kapsayıcı hizmeti için Orchestrator türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="757a1-133">Bu parametre için kabul edilebilir değerler: VSEÇCOS ve Snormal.</span><span class="sxs-lookup"><span data-stu-id="757a1-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="757a1-134">-Serviceprincipalprofileclıtıd</span><span class="sxs-lookup"><span data-stu-id="757a1-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="757a1-135">Sorumlu profil istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="757a1-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="757a1-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="757a1-137">Temel profil gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="757a1-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="757a1-138">-SshPublicKey</span></span>
<span data-ttu-id="757a1-139">Linux tabanlı kapsayıcı hizmeti için SSH ortak anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="757a1-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="757a1-140">-Tag</span></span>
<span data-ttu-id="757a1-141">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="757a1-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="757a1-142">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="757a1-142">For example:</span></span>

<span data-ttu-id="757a1-143">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="757a1-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="757a1-144">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="757a1-144">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="757a1-145">Bu yapılandırmanın kapsayıcı hizmeti sanal makinesi için tanılamayı etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="757a1-145">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="757a1-146">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="757a1-146">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="757a1-147">Windows işletim sistemini kullanan bir kapsayıcı hizmeti için yönetici parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-147">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="757a1-148">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="757a1-148">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="757a1-149">Windows işletim sistemini kullanan bir kapsayıcı hizmeti için yönetici kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="757a1-149">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="757a1-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="757a1-150">-Confirm</span></span>
<span data-ttu-id="757a1-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="757a1-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="757a1-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757a1-152">-WhatIf</span></span>
<span data-ttu-id="757a1-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="757a1-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="757a1-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="757a1-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="757a1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757a1-155">CommonParameters</span></span>
<span data-ttu-id="757a1-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="757a1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757a1-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="757a1-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757a1-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="757a1-158">INPUTS</span></span>

### <span data-ttu-id="757a1-159">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="757a1-159">None</span></span>
<span data-ttu-id="757a1-160">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="757a1-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="757a1-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="757a1-161">OUTPUTS</span></span>

### <span data-ttu-id="757a1-162">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="757a1-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="757a1-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="757a1-163">NOTES</span></span>

## <span data-ttu-id="757a1-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="757a1-164">RELATED LINKS</span></span>

[<span data-ttu-id="757a1-165">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="757a1-165">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="757a1-166">Yeni-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="757a1-166">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)
