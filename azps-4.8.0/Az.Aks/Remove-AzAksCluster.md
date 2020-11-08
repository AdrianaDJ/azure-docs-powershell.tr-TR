---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266162"
---
# <span data-ttu-id="32d20-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="32d20-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="32d20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32d20-102">SYNOPSIS</span></span>
<span data-ttu-id="32d20-103">Yönetilen Kubernetes kümesini silme.</span><span class="sxs-lookup"><span data-stu-id="32d20-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="32d20-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32d20-104">SYNTAX</span></span>

### <span data-ttu-id="32d20-105">GroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="32d20-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32d20-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="32d20-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32d20-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="32d20-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32d20-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="32d20-108">DESCRIPTION</span></span>
<span data-ttu-id="32d20-109">Yönetilen Kubernetes kümesini silme.</span><span class="sxs-lookup"><span data-stu-id="32d20-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="32d20-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32d20-110">EXAMPLES</span></span>

### <span data-ttu-id="32d20-111">Varolan bir yönetilen Kubernetes kümesini silme</span><span class="sxs-lookup"><span data-stu-id="32d20-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="32d20-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32d20-112">PARAMETERS</span></span>

### <span data-ttu-id="32d20-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="32d20-113">-AsJob</span></span>
<span data-ttu-id="32d20-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="32d20-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32d20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d20-115">-DefaultProfile</span></span>
<span data-ttu-id="32d20-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32d20-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32d20-117">-Force</span><span class="sxs-lookup"><span data-stu-id="32d20-117">-Force</span></span>
<span data-ttu-id="32d20-118">Yönetilen Kubernetes kümesini sormadan kaldır</span><span class="sxs-lookup"><span data-stu-id="32d20-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="32d20-119">-ID</span><span class="sxs-lookup"><span data-stu-id="32d20-119">-Id</span></span>
<span data-ttu-id="32d20-120">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="32d20-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32d20-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32d20-121">-InputObject</span></span>
<span data-ttu-id="32d20-122">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="32d20-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32d20-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="32d20-123">-Name</span></span>
<span data-ttu-id="32d20-124">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="32d20-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d20-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="32d20-125">-PassThru</span></span>
<span data-ttu-id="32d20-126">Silme işlemi başarılıysa doğru verir</span><span class="sxs-lookup"><span data-stu-id="32d20-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="32d20-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32d20-127">-ResourceGroupName</span></span>
<span data-ttu-id="32d20-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="32d20-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d20-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="32d20-129">-Confirm</span></span>
<span data-ttu-id="32d20-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="32d20-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32d20-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32d20-131">-WhatIf</span></span>
<span data-ttu-id="32d20-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32d20-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32d20-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="32d20-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32d20-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d20-134">CommonParameters</span></span>
<span data-ttu-id="32d20-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32d20-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d20-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="32d20-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d20-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32d20-137">INPUTS</span></span>

### <span data-ttu-id="32d20-138">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="32d20-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="32d20-139">System. String</span><span class="sxs-lookup"><span data-stu-id="32d20-139">System.String</span></span>

## <span data-ttu-id="32d20-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32d20-140">OUTPUTS</span></span>

### <span data-ttu-id="32d20-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32d20-141">System.Boolean</span></span>

## <span data-ttu-id="32d20-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32d20-142">NOTES</span></span>

## <span data-ttu-id="32d20-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32d20-143">RELATED LINKS</span></span>
