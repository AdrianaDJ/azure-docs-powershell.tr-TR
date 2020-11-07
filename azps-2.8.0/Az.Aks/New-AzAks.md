---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: 1de3cef0d14213a52873742f9bf878aaa545e8bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753682"
---
# <span data-ttu-id="e61aa-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="e61aa-101">New-AzAks</span></span>

## <span data-ttu-id="e61aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e61aa-102">SYNOPSIS</span></span>
<span data-ttu-id="e61aa-103">Yeni bir yönetilen Kubernetes kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e61aa-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e61aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e61aa-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e61aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e61aa-105">DESCRIPTION</span></span>

<span data-ttu-id="e61aa-106">Yeni bir yönetilen Kubernetes kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e61aa-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e61aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e61aa-107">EXAMPLES</span></span>

### <span data-ttu-id="e61aa-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e61aa-108">Example 1</span></span>

<span data-ttu-id="e61aa-109">Varsayılan params ile yeni bir yönetilen Kubernetes kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e61aa-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="e61aa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e61aa-110">PARAMETERS</span></span>

### <span data-ttu-id="e61aa-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="e61aa-111">-AdminUserName</span></span>
<span data-ttu-id="e61aa-112">Linux sanal makinelerinin Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="e61aa-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="e61aa-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="e61aa-113">-AsJob</span></span>
<span data-ttu-id="e61aa-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e61aa-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e61aa-115">-Clientidanvseçsecret</span><span class="sxs-lookup"><span data-stu-id="e61aa-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="e61aa-116">AAD uygulaması/hizmet sorumlusu ile ilişkilendirilmiş istemci kimliği ve istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="e61aa-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="e61aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e61aa-117">-DefaultProfile</span></span>
<span data-ttu-id="e61aa-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e61aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e61aa-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="e61aa-119">-DnsNamePrefix</span></span>
<span data-ttu-id="e61aa-120">Kümenin DNS adı öneki.</span><span class="sxs-lookup"><span data-stu-id="e61aa-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="e61aa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e61aa-121">-Force</span></span>
<span data-ttu-id="e61aa-122">Zaten var olsa bile küme oluştur</span><span class="sxs-lookup"><span data-stu-id="e61aa-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="e61aa-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="e61aa-123">-KubernetesVersion</span></span>
<span data-ttu-id="e61aa-124">Küme oluştururken kullanılacak Kubernetes sürümü.</span><span class="sxs-lookup"><span data-stu-id="e61aa-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="e61aa-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="e61aa-125">-Location</span></span>
<span data-ttu-id="e61aa-126">Kümenin Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="e61aa-126">Azure location for the cluster.</span></span>
<span data-ttu-id="e61aa-127">Kaynak grubunun konumunu varsayılan olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="e61aa-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="e61aa-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="e61aa-128">-Name</span></span>
<span data-ttu-id="e61aa-129">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="e61aa-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="e61aa-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="e61aa-130">-NodeCount</span></span>
<span data-ttu-id="e61aa-131">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="e61aa-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="e61aa-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="e61aa-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="e61aa-133">Düğüm havuzundaki her düğümün işletim sistemi diskinin boyutu.</span><span class="sxs-lookup"><span data-stu-id="e61aa-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="e61aa-134">En az 30 GB.</span><span class="sxs-lookup"><span data-stu-id="e61aa-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="e61aa-135">-Edevmboyut</span><span class="sxs-lookup"><span data-stu-id="e61aa-135">-NodeVmSize</span></span>
<span data-ttu-id="e61aa-136">Sanal makinenin boyutu.</span><span class="sxs-lookup"><span data-stu-id="e61aa-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="e61aa-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e61aa-137">-ResourceGroupName</span></span>
<span data-ttu-id="e61aa-138">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e61aa-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="e61aa-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="e61aa-139">-SshKeyValue</span></span>
<span data-ttu-id="e61aa-140">SSH anahtar dosyası veya anahtar dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="e61aa-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="e61aa-141">{HOME}/.ssh/id_rsa. pub varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="e61aa-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="e61aa-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e61aa-142">-Tag</span></span>
<span data-ttu-id="e61aa-143">Kaynağa uygulanacak Etiketler</span><span class="sxs-lookup"><span data-stu-id="e61aa-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="e61aa-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="e61aa-144">-Confirm</span></span>
<span data-ttu-id="e61aa-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e61aa-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e61aa-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e61aa-146">-WhatIf</span></span>
<span data-ttu-id="e61aa-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e61aa-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e61aa-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e61aa-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e61aa-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e61aa-149">CommonParameters</span></span>
<span data-ttu-id="e61aa-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e61aa-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e61aa-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e61aa-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e61aa-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e61aa-152">INPUTS</span></span>

### <span data-ttu-id="e61aa-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e61aa-153">None</span></span>

## <span data-ttu-id="e61aa-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e61aa-154">OUTPUTS</span></span>

### <span data-ttu-id="e61aa-155">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e61aa-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="e61aa-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e61aa-156">NOTES</span></span>

## <span data-ttu-id="e61aa-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e61aa-157">RELATED LINKS</span></span>
