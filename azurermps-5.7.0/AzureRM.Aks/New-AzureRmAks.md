---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: ed68271ae29c7af0219fa08d1c342b636d7d3fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764500"
---
# <span data-ttu-id="a2ed5-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="a2ed5-101">New-AzureRmAks</span></span>

## <span data-ttu-id="a2ed5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ed5-103">Yeni bir yönetilen Kubernetes kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2ed5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2ed5-104">SYNTAX</span></span>

```
New-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-Force] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2ed5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2ed5-105">DESCRIPTION</span></span>
<span data-ttu-id="a2ed5-106">Yeni bir yönetilen Kubernetes kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="a2ed5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2ed5-107">EXAMPLES</span></span>

### <span data-ttu-id="a2ed5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a2ed5-108">Example 1</span></span>
<span data-ttu-id="a2ed5-109">Varsayılan params ile yeni bir yönetilen Kubernetes kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a2ed5-109">Create a new managed Kubernetes cluster with default params</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="a2ed5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2ed5-110">PARAMETERS</span></span>

### <span data-ttu-id="a2ed5-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="a2ed5-111">-AdminUserName</span></span>
<span data-ttu-id="a2ed5-112">Linux sanal makinelerinin Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-112">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a2ed5-113">-AsJob</span></span>
<span data-ttu-id="a2ed5-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a2ed5-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-115">-Clientidanvseçsecret</span><span class="sxs-lookup"><span data-stu-id="a2ed5-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="a2ed5-116">AAD uygulaması/hizmet sorumlusu ile ilişkilendirilmiş istemci kimliği ve istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ed5-117">-DefaultProfile</span></span>
<span data-ttu-id="a2ed5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2ed5-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="a2ed5-119">-DnsNamePrefix</span></span>
<span data-ttu-id="a2ed5-120">Kümenin DNS adı öneki.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-120">The DNS name prefix for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a2ed5-121">-Force</span></span>
<span data-ttu-id="a2ed5-122">Zaten var olsa bile küme oluştur</span><span class="sxs-lookup"><span data-stu-id="a2ed5-122">Create cluster even if it already exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="a2ed5-123">-KubernetesVersion</span></span>
<span data-ttu-id="a2ed5-124">Küme oluştururken kullanılacak Kubernetes sürümü.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-124">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="a2ed5-125">-Location</span></span>
<span data-ttu-id="a2ed5-126">Kümenin Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-126">Azure location for the cluster.</span></span>
<span data-ttu-id="a2ed5-127">Kaynak grubunun konumunu varsayılan olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-127">Defaults to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="a2ed5-128">-Name</span></span>
<span data-ttu-id="a2ed5-129">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="a2ed5-130">-NodeCount</span></span>
<span data-ttu-id="a2ed5-131">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="a2ed5-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="a2ed5-133">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-133">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-134">-Edevmboyut</span><span class="sxs-lookup"><span data-stu-id="a2ed5-134">-NodeVmSize</span></span>
<span data-ttu-id="a2ed5-135">Sanal makinenin boyutu.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-135">The size of the Virtual Machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ed5-136">-ResourceGroupName</span></span>
<span data-ttu-id="a2ed5-137">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-138">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="a2ed5-138">-SshKeyValue</span></span>
<span data-ttu-id="a2ed5-139">SSH anahtar dosyası veya anahtar dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-139">SSH key file value or key file path.</span></span>
<span data-ttu-id="a2ed5-140">{HOME}/.ssh/id_rsa. pub varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-140">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a2ed5-141">-Tag</span></span>
<span data-ttu-id="a2ed5-142">Kaynağa uygulanacak Etiketler</span><span class="sxs-lookup"><span data-stu-id="a2ed5-142">Tags to be applied to the resource</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ed5-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2ed5-143">-Confirm</span></span>
<span data-ttu-id="a2ed5-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2ed5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2ed5-145">-WhatIf</span></span>
<span data-ttu-id="a2ed5-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2ed5-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2ed5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ed5-148">CommonParameters</span></span>
<span data-ttu-id="a2ed5-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2ed5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ed5-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2ed5-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ed5-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2ed5-151">INPUTS</span></span>

### <span data-ttu-id="a2ed5-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a2ed5-152">None</span></span>

## <span data-ttu-id="a2ed5-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2ed5-153">OUTPUTS</span></span>

### <span data-ttu-id="a2ed5-154">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="a2ed5-154">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="a2ed5-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2ed5-155">NOTES</span></span>

## <span data-ttu-id="a2ed5-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2ed5-156">RELATED LINKS</span></span>
