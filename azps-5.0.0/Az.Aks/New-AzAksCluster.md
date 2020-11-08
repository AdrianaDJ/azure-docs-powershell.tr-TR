---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277111"
---
# <span data-ttu-id="65321-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="65321-101">New-AzAksCluster</span></span>

## <span data-ttu-id="65321-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65321-102">SYNOPSIS</span></span>
<span data-ttu-id="65321-103">Yeni bir yönetilen Kubernetes kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="65321-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="65321-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65321-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
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

## <span data-ttu-id="65321-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="65321-105">DESCRIPTION</span></span>

<span data-ttu-id="65321-106">Yeni bir Azure Kubernetes hizmet (AKS) kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="65321-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="65321-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65321-107">EXAMPLES</span></span>

### <span data-ttu-id="65321-108">Varsayılan params ile yeni bir.</span><span class="sxs-lookup"><span data-stu-id="65321-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="65321-109">Windows Server kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="65321-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="65321-110">Bir noktada Windows Server kapsayıcısı oluşturmak için, AKS oluştururken en az dört parametre belirtmeniz gerekir `NetworkPlugin` ve ve `NodeVmSetType` `azure` `VirtualMachineScaleSets`</span><span class="sxs-lookup"><span data-stu-id="65321-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="65321-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65321-111">PARAMETERS</span></span>

### <span data-ttu-id="65321-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="65321-112">-AcrNameToAttach</span></span>
<span data-ttu-id="65321-113">' Acrpull ' rolüne, (örneğin, myacr)</span><span class="sxs-lookup"><span data-stu-id="65321-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="65321-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="65321-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="65321-115">Küme oluşturulduğunda etkinleştirilecek adlar.</span><span class="sxs-lookup"><span data-stu-id="65321-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="65321-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="65321-116">-AsJob</span></span>
<span data-ttu-id="65321-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="65321-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65321-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65321-118">-DefaultProfile</span></span>
<span data-ttu-id="65321-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65321-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65321-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="65321-120">-DnsNamePrefix</span></span>
<span data-ttu-id="65321-121">Kümenin DNS adı öneki.</span><span class="sxs-lookup"><span data-stu-id="65321-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="65321-122">Kullanıcılar Windows kapsayıcısını eklemeyi planalıyorsa uzunluk <= 9 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="65321-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="65321-123">-Enablenodeautoölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="65321-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="65321-124">Otomatik gizleme</span><span class="sxs-lookup"><span data-stu-id="65321-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="65321-125">-Enablertzb</span><span class="sxs-lookup"><span data-stu-id="65321-125">-EnableRbac</span></span>
<span data-ttu-id="65321-126">Kubernetes Role-Based erişimi etkinleştirilip etkinleştirilmeyeceğini</span><span class="sxs-lookup"><span data-stu-id="65321-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="65321-127">-Force</span><span class="sxs-lookup"><span data-stu-id="65321-127">-Force</span></span>
<span data-ttu-id="65321-128">Zaten var olsa bile küme oluştur</span><span class="sxs-lookup"><span data-stu-id="65321-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="65321-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="65321-129">-GenerateSshKey</span></span>
<span data-ttu-id="65321-130">{HOME}/.ssh/id_rsa için SSH anahtar dosyası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="65321-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="65321-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="65321-131">-KubernetesVersion</span></span>
<span data-ttu-id="65321-132">Küme oluştururken kullanılacak Kubernetes sürümü.</span><span class="sxs-lookup"><span data-stu-id="65321-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="65321-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="65321-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="65321-134">Linux sanal makinelerinin Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="65321-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="65321-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="65321-135">-LoadBalancerSku</span></span>
<span data-ttu-id="65321-136">Yönetilen kümenin yük dengeleyici SKU 'su.</span><span class="sxs-lookup"><span data-stu-id="65321-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="65321-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="65321-137">-Location</span></span>
<span data-ttu-id="65321-138">Kümenin Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="65321-138">Azure location for the cluster.</span></span>
<span data-ttu-id="65321-139">Kaynak grubunun konumunu varsayılan olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="65321-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="65321-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="65321-140">-Name</span></span>
<span data-ttu-id="65321-141">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="65321-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="65321-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="65321-142">-NetworkPlugin</span></span>
<span data-ttu-id="65321-143">Kubernetes ağı oluşturmak için kullanılan ağ eklentisi.</span><span class="sxs-lookup"><span data-stu-id="65321-143">Network plugin used for building Kubernetes network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: azure
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65321-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="65321-144">-NodeCount</span></span>
<span data-ttu-id="65321-145">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="65321-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="65321-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="65321-146">-NodeMaxCount</span></span>
<span data-ttu-id="65321-147">Otomatik ölçeklendirme için en fazla düğüm sayısı</span><span class="sxs-lookup"><span data-stu-id="65321-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="65321-148">-Nodemaxpod sayısı</span><span class="sxs-lookup"><span data-stu-id="65321-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="65321-149">Düğümde çalıştırılabilecek en fazla düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="65321-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="65321-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="65321-150">-NodeMinCount</span></span>
<span data-ttu-id="65321-151">Otomatik ölçeklendirme için en az düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="65321-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="65321-152">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="65321-152">-NodeName</span></span>
<span data-ttu-id="65321-153">Abonelik ve kaynak grubu bağlamında aracı havuzu profilinin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="65321-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="65321-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="65321-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="65321-155">Düğüm havuzundaki her düğümün işletim sistemi diskinin boyutu.</span><span class="sxs-lookup"><span data-stu-id="65321-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="65321-156">En az 30 GB.</span><span class="sxs-lookup"><span data-stu-id="65321-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="65321-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="65321-157">-NodePoolMode</span></span>
<span data-ttu-id="65321-158">NodePoolMode bir düğüm havuzu için temsil eder.</span><span class="sxs-lookup"><span data-stu-id="65321-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="65321-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="65321-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="65321-160">Düşük öncelikli sanal makine ölçek kümesi için çıkarma ilkesini belirtmek amacıyla kullanılan ScaleSetEvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="65321-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="65321-161">Varsayılan olarak silinir.</span><span class="sxs-lookup"><span data-stu-id="65321-161">Default to Delete.</span></span>

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

### <span data-ttu-id="65321-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="65321-162">-NodeSetPriority</span></span>
<span data-ttu-id="65321-163">Sanal makine ölçek kümesi önceliğini belirtmek için kullanılacak ScaleSetPriority.</span><span class="sxs-lookup"><span data-stu-id="65321-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="65321-164">Normal olarak.</span><span class="sxs-lookup"><span data-stu-id="65321-164">Default to regular.</span></span>

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

### <span data-ttu-id="65321-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="65321-165">-NodeVmSetType</span></span>
<span data-ttu-id="65321-166">AgentPoolType, bir aracı havuzunun türlerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="65321-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="65321-167">Olası değerler: ' VirtualMachineScaleSets ', ' kullanılabilirlik ayarı '</span><span class="sxs-lookup"><span data-stu-id="65321-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: VirtualMachineScaleSets
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65321-168">-Edevmboyut</span><span class="sxs-lookup"><span data-stu-id="65321-168">-NodeVmSize</span></span>
<span data-ttu-id="65321-169">Sanal makinenin boyutu.</span><span class="sxs-lookup"><span data-stu-id="65321-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="65321-170">Varsayılan değer Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="65321-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="65321-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="65321-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="65321-172">VNet alt Netid, VNet 'in alt ağ tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65321-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="65321-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65321-173">-ResourceGroupName</span></span>
<span data-ttu-id="65321-174">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="65321-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="65321-175">-Serviceprenalidancısecret</span><span class="sxs-lookup"><span data-stu-id="65321-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="65321-176">AAD uygulaması/hizmet sorumlusu ile ilişkilendirilmiş istemci kimliği ve istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="65321-176">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65321-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="65321-177">-SshKeyValue</span></span>
<span data-ttu-id="65321-178">SSH anahtar dosyası veya anahtar dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="65321-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="65321-179">{HOME}/.ssh/id_rsa. pub varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="65321-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="65321-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="65321-180">-SubnetName</span></span>
<span data-ttu-id="65321-181">VirtualNode eklentisi 'nin alt ağ adı.</span><span class="sxs-lookup"><span data-stu-id="65321-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="65321-182">Etiketli</span><span class="sxs-lookup"><span data-stu-id="65321-182">-Tag</span></span>
<span data-ttu-id="65321-183">Kaynağa uygulanacak Etiketler</span><span class="sxs-lookup"><span data-stu-id="65321-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="65321-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="65321-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="65321-185">Windows VM 'Ler için kullanılacak Yönetici Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="65321-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="65321-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="65321-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="65321-187">Windows VM 'Ler için kullanılacak yönetici parolası, uzunluğunun en az 12, en az bir küçük harf karakter, yani bir de bir `[a-z]` `[A-Z]` özel karakteri vardır `[!@#$%^&_()]` .</span><span class="sxs-lookup"><span data-stu-id="65321-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

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

### <span data-ttu-id="65321-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="65321-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="65321-189">Izleme eklentisi çalışma alanının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="65321-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="65321-190">-Onay</span><span class="sxs-lookup"><span data-stu-id="65321-190">-Confirm</span></span>
<span data-ttu-id="65321-191">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65321-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65321-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65321-192">-WhatIf</span></span>
<span data-ttu-id="65321-193">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65321-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65321-194">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65321-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65321-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65321-195">CommonParameters</span></span>
<span data-ttu-id="65321-196">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65321-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65321-197">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="65321-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65321-198">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65321-198">INPUTS</span></span>

### <span data-ttu-id="65321-199">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="65321-199">None</span></span>

## <span data-ttu-id="65321-200">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65321-200">OUTPUTS</span></span>

### <span data-ttu-id="65321-201">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="65321-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="65321-202">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65321-202">NOTES</span></span>

## <span data-ttu-id="65321-203">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65321-203">RELATED LINKS</span></span>
