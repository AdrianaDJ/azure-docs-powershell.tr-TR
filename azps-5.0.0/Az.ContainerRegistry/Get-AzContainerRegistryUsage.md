---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 691d8cf006e720d706d2473f76ff8660927e73ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275582"
---
# <span data-ttu-id="b27ae-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="b27ae-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="b27ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b27ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b27ae-103">Azure kapsayıcısı kayıt defterinin kullanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="b27ae-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="b27ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b27ae-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b27ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b27ae-105">DESCRIPTION</span></span>
<span data-ttu-id="b27ae-106">Azure kapsayıcısı kayıt defterinin kullanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="b27ae-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="b27ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b27ae-107">EXAMPLES</span></span>

### <span data-ttu-id="b27ae-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b27ae-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="b27ae-109">Azure kapsayıcısı kayıt defterinin kullanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="b27ae-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="b27ae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b27ae-110">PARAMETERS</span></span>

### <span data-ttu-id="b27ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27ae-111">-DefaultProfile</span></span>
<span data-ttu-id="b27ae-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b27ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b27ae-113">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b27ae-113">-RegistryName</span></span>
<span data-ttu-id="b27ae-114">Hedef kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="b27ae-114">Target registry name.</span></span>

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

### <span data-ttu-id="b27ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b27ae-115">-ResourceGroupName</span></span>
<span data-ttu-id="b27ae-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b27ae-116">Resource group name.</span></span>

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

### <span data-ttu-id="b27ae-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27ae-117">CommonParameters</span></span>
<span data-ttu-id="b27ae-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b27ae-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27ae-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b27ae-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27ae-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b27ae-120">INPUTS</span></span>

### <span data-ttu-id="b27ae-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b27ae-121">System.String</span></span>

## <span data-ttu-id="b27ae-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b27ae-122">OUTPUTS</span></span>

### <span data-ttu-id="b27ae-123">Microsoft. Azure. Commands. ContainerRegistry. model. PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="b27ae-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="b27ae-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b27ae-124">NOTES</span></span>

## <span data-ttu-id="b27ae-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b27ae-125">RELATED LINKS</span></span>
