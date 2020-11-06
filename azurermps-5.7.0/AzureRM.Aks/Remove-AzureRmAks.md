---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/remove-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
ms.openlocfilehash: 1843322f702f8c43f97f1cf64c9d9f5b92d419bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592528"
---
# <span data-ttu-id="a0ec8-101">Remove-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="a0ec8-101">Remove-AzureRmAks</span></span>

## <span data-ttu-id="a0ec8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ec8-103">Yönetilen Kubernetes kümesini silme.</span><span class="sxs-lookup"><span data-stu-id="a0ec8-103">Delete a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0ec8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0ec8-104">SYNTAX</span></span>

### <span data-ttu-id="a0ec8-105">GroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0ec8-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0ec8-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="a0ec8-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0ec8-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="a0ec8-107">IdParameterSet</span></span>
```
Remove-AzureRmAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0ec8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0ec8-108">DESCRIPTION</span></span>
<span data-ttu-id="a0ec8-109">Yönetilen Kubernetes kümesini silme.</span><span class="sxs-lookup"><span data-stu-id="a0ec8-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="a0ec8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0ec8-110">EXAMPLES</span></span>

### <span data-ttu-id="a0ec8-111">Varolan bir yönetilen Kubernetes kümesini silme</span><span class="sxs-lookup"><span data-stu-id="a0ec8-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="a0ec8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0ec8-112">PARAMETERS</span></span>

### <span data-ttu-id="a0ec8-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a0ec8-113">-AsJob</span></span>
<span data-ttu-id="a0ec8-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a0ec8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0ec8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ec8-115">-DefaultProfile</span></span>
<span data-ttu-id="a0ec8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0ec8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0ec8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a0ec8-117">-Force</span></span>
<span data-ttu-id="a0ec8-118">Yönetilen Kubernetes kümesini sormadan kaldır</span><span class="sxs-lookup"><span data-stu-id="a0ec8-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="a0ec8-119">-ID</span><span class="sxs-lookup"><span data-stu-id="a0ec8-119">-Id</span></span>
<span data-ttu-id="a0ec8-120">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="a0ec8-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ec8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0ec8-121">-InputObject</span></span>
<span data-ttu-id="a0ec8-122">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a0ec8-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ec8-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0ec8-123">-Name</span></span>
<span data-ttu-id="a0ec8-124">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="a0ec8-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ec8-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a0ec8-125">-PassThru</span></span>
<span data-ttu-id="a0ec8-126">Silme işlemi başarılıysa doğru verir</span><span class="sxs-lookup"><span data-stu-id="a0ec8-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="a0ec8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ec8-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0ec8-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a0ec8-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ec8-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0ec8-129">-Confirm</span></span>
<span data-ttu-id="a0ec8-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0ec8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0ec8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0ec8-131">-WhatIf</span></span>
<span data-ttu-id="a0ec8-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0ec8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0ec8-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0ec8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0ec8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ec8-134">CommonParameters</span></span>
<span data-ttu-id="a0ec8-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0ec8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ec8-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0ec8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ec8-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0ec8-137">INPUTS</span></span>

### <span data-ttu-id="a0ec8-138">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="a0ec8-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="a0ec8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a0ec8-139">System.String</span></span>

## <span data-ttu-id="a0ec8-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0ec8-140">OUTPUTS</span></span>

### <span data-ttu-id="a0ec8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0ec8-141">System.Boolean</span></span>

## <span data-ttu-id="a0ec8-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0ec8-142">NOTES</span></span>

## <span data-ttu-id="a0ec8-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0ec8-143">RELATED LINKS</span></span>
