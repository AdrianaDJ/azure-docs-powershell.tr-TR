---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: f7a3479fb7fd70c47d5d4d3b80004cb25d9baa0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266173"
---
# <span data-ttu-id="15a1b-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="15a1b-101">New-AzAksCluster</span></span>

## <span data-ttu-id="15a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="15a1b-103">Yeni bir yönetilen Kubernetes kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="15a1b-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="15a1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15a1b-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeOsType <String>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
 [-NodeScaleSetEvictionPolicy <String>] [-AddOnNameToBeEnabled <String[]>] [-WorkspaceResourceId <String>]
 [-SubnetName <String>] [-AcrNameToAttach <String>] [-EnableRbac] [-WindowsProfileAdminUserName <String>]
 [-WindowsProfileAdminUserPassword <SecureString>] [-NetworkPlugin <String>] [-LoadBalancerSku <String>]
 [-ResourceGroupName] <String> [-Name] <String> [[-ServicePrincipalIdAndSecret] <PSCredential>]
 [-Location <String>] [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>]
 [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a1b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15a1b-105">DESCRIPTION</span></span>

<span data-ttu-id="15a1b-106">Yeni bir Azure Kubernetes hizmet (AKS) kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="15a1b-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="15a1b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15a1b-107">EXAMPLES</span></span>

### <span data-ttu-id="15a1b-108">Varsayılan params ile yeni bir.</span><span class="sxs-lookup"><span data-stu-id="15a1b-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="15a1b-109">Windows Server kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="15a1b-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="15a1b-110">Bir noktada Windows Server kapsayıcısı oluşturmak için, AKS oluştururken en az dört parametre belirtmeniz gerekir `NetworkPlugin` ve ve `NodeVmSetType` `azure` `VirtualMachineScaleSets`</span><span class="sxs-lookup"><span data-stu-id="15a1b-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="15a1b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15a1b-111">PARAMETERS</span></span>

### <span data-ttu-id="15a1b-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="15a1b-112">-AcrNameToAttach</span></span>
<span data-ttu-id="15a1b-113">' Acrpull ' rolüne, (örneğin, myacr)</span><span class="sxs-lookup"><span data-stu-id="15a1b-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="15a1b-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="15a1b-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="15a1b-115">Küme oluşturulduğunda etkinleştirilecek adlar.</span><span class="sxs-lookup"><span data-stu-id="15a1b-115">Add-on names to be enabled when cluster is created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a1b-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="15a1b-116">-AsJob</span></span>
<span data-ttu-id="15a1b-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="15a1b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15a1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a1b-118">-DefaultProfile</span></span>
<span data-ttu-id="15a1b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15a1b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a1b-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="15a1b-120">-DnsNamePrefix</span></span>
<span data-ttu-id="15a1b-121">Kümenin DNS adı öneki.</span><span class="sxs-lookup"><span data-stu-id="15a1b-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="15a1b-122">Kullanıcılar Windows kapsayıcısını eklemeyi planalıyorsa uzunluk <= 9 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="15a1b-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="15a1b-123">-Enablenodeautoölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="15a1b-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="15a1b-124">Otomatik gizleme</span><span class="sxs-lookup"><span data-stu-id="15a1b-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="15a1b-125">-Enablertzb</span><span class="sxs-lookup"><span data-stu-id="15a1b-125">-EnableRbac</span></span>
<span data-ttu-id="15a1b-126">Kubernetes Role-Based erişimi etkinleştirilip etkinleştirilmeyeceğini</span><span class="sxs-lookup"><span data-stu-id="15a1b-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="15a1b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="15a1b-127">-Force</span></span>
<span data-ttu-id="15a1b-128">Zaten var olsa bile küme oluştur</span><span class="sxs-lookup"><span data-stu-id="15a1b-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="15a1b-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="15a1b-129">-GenerateSshKey</span></span>
<span data-ttu-id="15a1b-130">{HOME}/.ssh/id_rsa için SSH anahtar dosyası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="15a1b-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="15a1b-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="15a1b-131">-KubernetesVersion</span></span>
<span data-ttu-id="15a1b-132">Küme oluştururken kullanılacak Kubernetes sürümü.</span><span class="sxs-lookup"><span data-stu-id="15a1b-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="15a1b-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="15a1b-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="15a1b-134">Linux sanal makinelerinin Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="15a1b-134">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a1b-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="15a1b-135">-LoadBalancerSku</span></span>
<span data-ttu-id="15a1b-136">Yönetilen kümenin yük dengeleyici SKU 'su.</span><span class="sxs-lookup"><span data-stu-id="15a1b-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="15a1b-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="15a1b-137">-Location</span></span>
<span data-ttu-id="15a1b-138">Kümenin Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="15a1b-138">Azure location for the cluster.</span></span>
<span data-ttu-id="15a1b-139">Kaynak grubunun konumunu varsayılan olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="15a1b-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="15a1b-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="15a1b-140">-Name</span></span>
<span data-ttu-id="15a1b-141">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="15a1b-141">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a1b-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="15a1b-142">-NetworkPlugin</span></span>
<span data-ttu-id="15a1b-143">Kubernetes ağı oluşturmak için kullanılan ağ eklentisi.</span><span class="sxs-lookup"><span data-stu-id="15a1b-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="15a1b-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="15a1b-144">-NodeCount</span></span>
<span data-ttu-id="15a1b-145">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="15a1b-145">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a1b-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="15a1b-146">-NodeMaxCount</span></span>
<span data-ttu-id="15a1b-147">Otomatik ölçeklendirme için en fazla düğüm sayısı</span><span class="sxs-lookup"><span data-stu-id="15a1b-147">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a1b-148">-Nodemaxpod sayısı</span><span class="sxs-lookup"><span data-stu-id="15a1b-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="15a1b-149">Düğümde çalıştırılabilecek en fazla düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="15a1b-149">Maximum number of pods that can run on node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a1b-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="15a1b-150">-NodeMinCount</span></span>
<span data-ttu-id="15a1b-151">Otomatik ölçeklendirme için en az düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="15a1b-151">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a1b-152">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="15a1b-152">-NodeName</span></span>
<span data-ttu-id="15a1b-153">Abonelik ve kaynak grubu bağlamında aracı havuzu profilinin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="15a1b-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="15a1b-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="15a1b-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="15a1b-155">Düğüm havuzundaki her düğümün işletim sistemi diskinin boyutu.</span><span class="sxs-lookup"><span data-stu-id="15a1b-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="15a1b-156">En az 30 GB.</span><span class="sxs-lookup"><span data-stu-id="15a1b-156">Minimum 30 GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a1b-157">-NodeOsType</span><span class="sxs-lookup"><span data-stu-id="15a1b-157">-NodeOsType</span></span>
<span data-ttu-id="15a1b-158">OS türünü belirtmek için kullanılacak OsType.</span><span class="sxs-lookup"><span data-stu-id="15a1b-158">OsType to be used to specify os type.</span></span> <span data-ttu-id="15a1b-159">Linux ve Windows 'tan seçim yapın.</span><span class="sxs-lookup"><span data-stu-id="15a1b-159">Choose from Linux and Windows.</span></span> <span data-ttu-id="15a1b-160">Linux.</span><span class="sxs-lookup"><span data-stu-id="15a1b-160">Default to Linux.</span></span>

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

### <span data-ttu-id="15a1b-161">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="15a1b-161">-NodePoolMode</span></span>
<span data-ttu-id="15a1b-162">NodePoolMode bir düğüm havuzu için temsil eder.</span><span class="sxs-lookup"><span data-stu-id="15a1b-162">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="15a1b-163">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="15a1b-163">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="15a1b-164">Düşük öncelikli sanal makine ölçek kümesi için çıkarma ilkesini belirtmek amacıyla kullanılan ScaleSetEvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="15a1b-164">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="15a1b-165">Varsayılan olarak silinir.</span><span class="sxs-lookup"><span data-stu-id="15a1b-165">Default to Delete.</span></span>

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

### <span data-ttu-id="15a1b-166">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="15a1b-166">-NodeSetPriority</span></span>
<span data-ttu-id="15a1b-167">Sanal makine ölçek kümesi önceliğini belirtmek için kullanılacak ScaleSetPriority.</span><span class="sxs-lookup"><span data-stu-id="15a1b-167">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="15a1b-168">Normal olarak.</span><span class="sxs-lookup"><span data-stu-id="15a1b-168">Default to regular.</span></span>

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

### <span data-ttu-id="15a1b-169">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="15a1b-169">-NodeVmSetType</span></span>
<span data-ttu-id="15a1b-170">AgentPoolType, bir aracı havuzunun türlerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="15a1b-170">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="15a1b-171">Olası değerler: ' VirtualMachineScaleSets ', ' kullanılabilirlik ayarı '</span><span class="sxs-lookup"><span data-stu-id="15a1b-171">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="15a1b-172">-Edevmboyut</span><span class="sxs-lookup"><span data-stu-id="15a1b-172">-NodeVmSize</span></span>
<span data-ttu-id="15a1b-173">Sanal makinenin boyutu.</span><span class="sxs-lookup"><span data-stu-id="15a1b-173">The size of the Virtual Machine.</span></span> <span data-ttu-id="15a1b-174">Varsayılan değer Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="15a1b-174">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="15a1b-175">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="15a1b-175">-NodeVnetSubnetID</span></span>
<span data-ttu-id="15a1b-176">VNet alt Netid, VNet 'in alt ağ tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15a1b-176">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="15a1b-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a1b-177">-ResourceGroupName</span></span>
<span data-ttu-id="15a1b-178">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="15a1b-178">Resource Group Name.</span></span>

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

### <span data-ttu-id="15a1b-179">-Serviceprenalidancısecret</span><span class="sxs-lookup"><span data-stu-id="15a1b-179">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="15a1b-180">AAD uygulaması/hizmet sorumlusu ile ilişkilendirilmiş istemci kimliği ve istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="15a1b-180">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClientIdAndSecret

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a1b-181">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="15a1b-181">-SshKeyValue</span></span>
<span data-ttu-id="15a1b-182">SSH anahtar dosyası veya anahtar dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="15a1b-182">SSH key file value or key file path.</span></span>
<span data-ttu-id="15a1b-183">{HOME}/.ssh/id_rsa. pub varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="15a1b-183">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a1b-184">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="15a1b-184">-SubnetName</span></span>
<span data-ttu-id="15a1b-185">VirtualNode eklentisi 'nin alt ağ adı.</span><span class="sxs-lookup"><span data-stu-id="15a1b-185">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="15a1b-186">Etiketli</span><span class="sxs-lookup"><span data-stu-id="15a1b-186">-Tag</span></span>
<span data-ttu-id="15a1b-187">Kaynağa uygulanacak Etiketler</span><span class="sxs-lookup"><span data-stu-id="15a1b-187">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="15a1b-188">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="15a1b-188">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="15a1b-189">Windows VM 'Ler için kullanılacak Yönetici Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="15a1b-189">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="15a1b-190">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="15a1b-190">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="15a1b-191">Windows VM 'Ler için kullanılacak yönetici parolası, uzunluğunun en az 12, en az bir küçük harf karakter, yani bir de bir `[a-z]` `[A-Z]` özel karakteri vardır `[!@#$%^&*()]` .</span><span class="sxs-lookup"><span data-stu-id="15a1b-191">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a1b-192">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="15a1b-192">-WorkspaceResourceId</span></span>
<span data-ttu-id="15a1b-193">Izleme eklentisi çalışma alanının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="15a1b-193">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="15a1b-194">-Onay</span><span class="sxs-lookup"><span data-stu-id="15a1b-194">-Confirm</span></span>
<span data-ttu-id="15a1b-195">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15a1b-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a1b-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a1b-196">-WhatIf</span></span>
<span data-ttu-id="15a1b-197">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15a1b-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a1b-198">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15a1b-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a1b-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a1b-199">CommonParameters</span></span>
<span data-ttu-id="15a1b-200">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15a1b-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a1b-201">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15a1b-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a1b-202">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15a1b-202">INPUTS</span></span>

### <span data-ttu-id="15a1b-203">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="15a1b-203">None</span></span>

## <span data-ttu-id="15a1b-204">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15a1b-204">OUTPUTS</span></span>

### <span data-ttu-id="15a1b-205">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="15a1b-205">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="15a1b-206">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15a1b-206">NOTES</span></span>

## <span data-ttu-id="15a1b-207">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15a1b-207">RELATED LINKS</span></span>
