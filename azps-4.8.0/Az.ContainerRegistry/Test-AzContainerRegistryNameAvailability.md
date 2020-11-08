---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267466"
---
# <span data-ttu-id="c3934-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c3934-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="c3934-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3934-102">SYNOPSIS</span></span>
<span data-ttu-id="c3934-103">Kapsayıcı kayıt defteri adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="c3934-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="c3934-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3934-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3934-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3934-105">DESCRIPTION</span></span>
<span data-ttu-id="c3934-106">Test-AzContainerRegistryNameAvailability cmdlet 'i, kapsayıcı kayıt defteri adının geçerli ve kullanılabilir olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="c3934-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="c3934-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3934-107">EXAMPLES</span></span>

### <span data-ttu-id="c3934-108">Örnek 1: kapsayıcı kayıt defteri adının uygunluk durumunu denetler</span><span class="sxs-lookup"><span data-stu-id="c3934-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="c3934-109">Bu komut, SomeRegistryName kapsayıcısı kayıt defteri adının kullanılabilirliğini denetler \` \` .</span><span class="sxs-lookup"><span data-stu-id="c3934-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="c3934-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3934-110">PARAMETERS</span></span>

### <span data-ttu-id="c3934-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3934-111">-DefaultProfile</span></span>
<span data-ttu-id="c3934-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c3934-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3934-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3934-113">-Name</span></span>
<span data-ttu-id="c3934-114">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="c3934-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3934-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3934-115">CommonParameters</span></span>
<span data-ttu-id="c3934-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3934-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3934-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c3934-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3934-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3934-118">INPUTS</span></span>

### <span data-ttu-id="c3934-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c3934-119">System.String</span></span>

## <span data-ttu-id="c3934-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3934-120">OUTPUTS</span></span>

### <span data-ttu-id="c3934-121">Microsoft. Azure. Management. ContainerRegistry. modeller. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="c3934-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="c3934-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3934-122">NOTES</span></span>

## <span data-ttu-id="c3934-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3934-123">RELATED LINKS</span></span>

[<span data-ttu-id="c3934-124">Yeni-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c3934-124">New-AzContainerRegistry</span></span>]()

