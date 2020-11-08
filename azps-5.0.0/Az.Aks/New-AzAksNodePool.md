---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277112"
---
# <span data-ttu-id="ba0e7-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="ba0e7-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="ba0e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba0e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ba0e7-103">Belirtilen kümede yeni bir düğüm havuzu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="ba0e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba0e7-104">SYNTAX</span></span>

### <span data-ttu-id="ba0e7-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba0e7-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba0e7-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba0e7-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba0e7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba0e7-107">DESCRIPTION</span></span>
<span data-ttu-id="ba0e7-108">Belirtilen kümede yeni bir düğüm havuzu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="ba0e7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba0e7-109">EXAMPLES</span></span>

### <span data-ttu-id="ba0e7-110">Varsayılan parametrelerle düğüm havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ba0e7-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="ba0e7-111">Windows Server kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="ba0e7-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="ba0e7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba0e7-112">PARAMETERS</span></span>

### <span data-ttu-id="ba0e7-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ba0e7-113">-ClusterName</span></span>
<span data-ttu-id="ba0e7-114">Yönetilen küme kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba0e7-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="ba0e7-115">-ClusterObject</span></span>
<span data-ttu-id="ba0e7-116">Düğüm havuzunun oluşturulacağı küme nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-116">Specify cluster object in which to create node pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba0e7-117">-Sayı</span><span class="sxs-lookup"><span data-stu-id="ba0e7-117">-Count</span></span>
<span data-ttu-id="ba0e7-118">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="ba0e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba0e7-119">-DefaultProfile</span></span>
<span data-ttu-id="ba0e7-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba0e7-121">-Enableautoölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="ba0e7-121">-EnableAutoScaling</span></span>
<span data-ttu-id="ba0e7-122">Otomatik gizleme</span><span class="sxs-lookup"><span data-stu-id="ba0e7-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="ba0e7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ba0e7-123">-Force</span></span>
<span data-ttu-id="ba0e7-124">Zaten var olsa bile düğüm Havuzu Oluştur</span><span class="sxs-lookup"><span data-stu-id="ba0e7-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="ba0e7-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="ba0e7-125">-KubernetesVersion</span></span>
<span data-ttu-id="ba0e7-126">Küme oluştururken kullanılacak Kubernetes sürümü.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="ba0e7-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ba0e7-127">-MaxCount</span></span>
<span data-ttu-id="ba0e7-128">Otomatik ölçeklendirme için en fazla düğüm sayısı</span><span class="sxs-lookup"><span data-stu-id="ba0e7-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="ba0e7-129">-Maxpod sayısı</span><span class="sxs-lookup"><span data-stu-id="ba0e7-129">-MaxPodCount</span></span>
<span data-ttu-id="ba0e7-130">Düğümde çalıştırılabilecek en fazla düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="ba0e7-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="ba0e7-131">-MinCount</span></span>
<span data-ttu-id="ba0e7-132">Otomatik ölçeklendirme için en az düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="ba0e7-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba0e7-133">-Name</span></span>
<span data-ttu-id="ba0e7-134">Düğüm havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="ba0e7-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="ba0e7-135">-OsDiskSize</span></span>
<span data-ttu-id="ba0e7-136">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="ba0e7-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="ba0e7-137">-OsType</span></span>
<span data-ttu-id="ba0e7-138">OS türünü belirtmek için kullanılacak OsType.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="ba0e7-139">Linux ve Windows 'tan seçim yapın.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="ba0e7-140">Linux.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-140">Default to Linux.</span></span>

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

### <span data-ttu-id="ba0e7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba0e7-141">-ResourceGroupName</span></span>
<span data-ttu-id="ba0e7-142">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-142">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba0e7-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba0e7-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="ba0e7-144">Düşük öncelikli sanal makine ölçek kümesi için çıkarma ilkesini belirtmek amacıyla kullanılan ScaleSetEvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="ba0e7-145">Varsayılan olarak silinir.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-145">Default to Delete.</span></span>

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

### <span data-ttu-id="ba0e7-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="ba0e7-146">-ScaleSetPriority</span></span>
<span data-ttu-id="ba0e7-147">Sanal makine ölçek kümesi önceliğini belirtmek için kullanılacak ScaleSetPriority.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="ba0e7-148">Normal olarak.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-148">Default to regular.</span></span>

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

### <span data-ttu-id="ba0e7-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="ba0e7-149">-VmSetType</span></span>
<span data-ttu-id="ba0e7-150">Düğüm havuzunun türlerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-150">Represents types of an node pool.</span></span>
<span data-ttu-id="ba0e7-151">Olası değerler: ' VirtualMachineScaleSets ', ' kullanılabilirlik ayarı '</span><span class="sxs-lookup"><span data-stu-id="ba0e7-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="ba0e7-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="ba0e7-152">-VmSize</span></span>
<span data-ttu-id="ba0e7-153">Sanal makinenin boyutu.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="ba0e7-154">Varsayılan değer Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="ba0e7-155">-Vnetsubnetıd</span><span class="sxs-lookup"><span data-stu-id="ba0e7-155">-VnetSubnetID</span></span>
<span data-ttu-id="ba0e7-156">VNet alt Netid, VNet 'in alt ağ tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="ba0e7-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba0e7-157">-Confirm</span></span>
<span data-ttu-id="ba0e7-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba0e7-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba0e7-159">-WhatIf</span></span>
<span data-ttu-id="ba0e7-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba0e7-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba0e7-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba0e7-162">CommonParameters</span></span>
<span data-ttu-id="ba0e7-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba0e7-164">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba0e7-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba0e7-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba0e7-165">INPUTS</span></span>

### <span data-ttu-id="ba0e7-166">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ba0e7-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ba0e7-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba0e7-167">OUTPUTS</span></span>

### <span data-ttu-id="ba0e7-168">Microsoft. Azure. Commands. aks. modeller. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="ba0e7-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="ba0e7-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba0e7-169">NOTES</span></span>

## <span data-ttu-id="ba0e7-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba0e7-170">RELATED LINKS</span></span>
