---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/remove-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
ms.openlocfilehash: 909121a78d09db7d15591a93db9479d0ccc8381b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592357"
---
# <span data-ttu-id="6c0ec-101">Remove-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="6c0ec-101">Remove-AzureRmAks</span></span>

## <span data-ttu-id="6c0ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0ec-103">Yönetilen Kubernetes kümesini silme.</span><span class="sxs-lookup"><span data-stu-id="6c0ec-103">Delete a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c0ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c0ec-104">SYNTAX</span></span>

### <span data-ttu-id="6c0ec-105">GroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6c0ec-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c0ec-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="6c0ec-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c0ec-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="6c0ec-107">IdParameterSet</span></span>
```
Remove-AzureRmAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c0ec-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c0ec-108">DESCRIPTION</span></span>
<span data-ttu-id="6c0ec-109">Yönetilen Kubernetes kümesini silme.</span><span class="sxs-lookup"><span data-stu-id="6c0ec-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="6c0ec-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c0ec-110">EXAMPLES</span></span>

### <span data-ttu-id="6c0ec-111">Varolan bir yönetilen Kubernetes kümesini silme</span><span class="sxs-lookup"><span data-stu-id="6c0ec-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="6c0ec-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c0ec-112">PARAMETERS</span></span>

### <span data-ttu-id="6c0ec-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="6c0ec-113">-AsJob</span></span>
<span data-ttu-id="6c0ec-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6c0ec-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c0ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0ec-115">-DefaultProfile</span></span>
<span data-ttu-id="6c0ec-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c0ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c0ec-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6c0ec-117">-Force</span></span>
<span data-ttu-id="6c0ec-118">Yönetilen Kubernetes kümesini sormadan kaldır</span><span class="sxs-lookup"><span data-stu-id="6c0ec-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="6c0ec-119">-ID</span><span class="sxs-lookup"><span data-stu-id="6c0ec-119">-Id</span></span>
<span data-ttu-id="6c0ec-120">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="6c0ec-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6c0ec-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c0ec-121">-InputObject</span></span>
<span data-ttu-id="6c0ec-122">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6c0ec-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6c0ec-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c0ec-123">-Name</span></span>
<span data-ttu-id="6c0ec-124">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="6c0ec-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6c0ec-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6c0ec-125">-PassThru</span></span>
<span data-ttu-id="6c0ec-126">Silme işlemi başarılıysa doğru verir</span><span class="sxs-lookup"><span data-stu-id="6c0ec-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="6c0ec-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c0ec-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c0ec-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6c0ec-128">Resource group name</span></span>

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

### <span data-ttu-id="6c0ec-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6c0ec-129">-Confirm</span></span>
<span data-ttu-id="6c0ec-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6c0ec-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c0ec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c0ec-131">-WhatIf</span></span>
<span data-ttu-id="6c0ec-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c0ec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c0ec-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6c0ec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c0ec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0ec-134">CommonParameters</span></span>
<span data-ttu-id="6c0ec-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c0ec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0ec-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c0ec-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0ec-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c0ec-137">INPUTS</span></span>

### <span data-ttu-id="6c0ec-138">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="6c0ec-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="6c0ec-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c0ec-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6c0ec-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6c0ec-140">System.String</span></span>

## <span data-ttu-id="6c0ec-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c0ec-141">OUTPUTS</span></span>

### <span data-ttu-id="6c0ec-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c0ec-142">System.Boolean</span></span>

## <span data-ttu-id="6c0ec-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c0ec-143">NOTES</span></span>

## <span data-ttu-id="6c0ec-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c0ec-144">RELATED LINKS</span></span>
