---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
ms.openlocfilehash: dc8b22697d606e827a0855a446d969ff2c90edc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751225"
---
# <span data-ttu-id="ef488-101">Remove-AzAks</span><span class="sxs-lookup"><span data-stu-id="ef488-101">Remove-AzAks</span></span>

## <span data-ttu-id="ef488-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef488-102">SYNOPSIS</span></span>
<span data-ttu-id="ef488-103">Yönetilen Kubernetes kümesini silme.</span><span class="sxs-lookup"><span data-stu-id="ef488-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ef488-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef488-104">SYNTAX</span></span>

### <span data-ttu-id="ef488-105">GroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ef488-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef488-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="ef488-106">InputObjectParameterSet</span></span>
```
Remove-AzAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef488-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="ef488-107">IdParameterSet</span></span>
```
Remove-AzAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef488-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef488-108">DESCRIPTION</span></span>
<span data-ttu-id="ef488-109">Yönetilen Kubernetes kümesini silme.</span><span class="sxs-lookup"><span data-stu-id="ef488-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ef488-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef488-110">EXAMPLES</span></span>

### <span data-ttu-id="ef488-111">Varolan bir yönetilen Kubernetes kümesini silme</span><span class="sxs-lookup"><span data-stu-id="ef488-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="ef488-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef488-112">PARAMETERS</span></span>

### <span data-ttu-id="ef488-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ef488-113">-AsJob</span></span>
<span data-ttu-id="ef488-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ef488-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef488-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef488-115">-DefaultProfile</span></span>
<span data-ttu-id="ef488-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ef488-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef488-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ef488-117">-Force</span></span>
<span data-ttu-id="ef488-118">Yönetilen Kubernetes kümesini sormadan kaldır</span><span class="sxs-lookup"><span data-stu-id="ef488-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="ef488-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ef488-119">-Id</span></span>
<span data-ttu-id="ef488-120">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="ef488-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ef488-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef488-121">-InputObject</span></span>
<span data-ttu-id="ef488-122">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ef488-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ef488-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="ef488-123">-Name</span></span>
<span data-ttu-id="ef488-124">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="ef488-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ef488-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ef488-125">-PassThru</span></span>
<span data-ttu-id="ef488-126">Silme işlemi başarılıysa doğru verir</span><span class="sxs-lookup"><span data-stu-id="ef488-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="ef488-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef488-127">-ResourceGroupName</span></span>
<span data-ttu-id="ef488-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ef488-128">Resource group name</span></span>

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

### <span data-ttu-id="ef488-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="ef488-129">-Confirm</span></span>
<span data-ttu-id="ef488-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ef488-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef488-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef488-131">-WhatIf</span></span>
<span data-ttu-id="ef488-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ef488-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef488-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ef488-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef488-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef488-134">CommonParameters</span></span>
<span data-ttu-id="ef488-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef488-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef488-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef488-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef488-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef488-137">INPUTS</span></span>

### <span data-ttu-id="ef488-138">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ef488-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="ef488-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ef488-139">System.String</span></span>

## <span data-ttu-id="ef488-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef488-140">OUTPUTS</span></span>

### <span data-ttu-id="ef488-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef488-141">System.Boolean</span></span>

## <span data-ttu-id="ef488-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef488-142">NOTES</span></span>

## <span data-ttu-id="ef488-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef488-143">RELATED LINKS</span></span>
