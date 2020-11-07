---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 4471835a1ff87a44722fc9e0dd51b0fa279410f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917147"
---
# <span data-ttu-id="8a763-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8a763-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="8a763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a763-102">SYNOPSIS</span></span>
<span data-ttu-id="8a763-103">Kapsayıcı kayıt defteri adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="8a763-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="8a763-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a763-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a763-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a763-105">DESCRIPTION</span></span>
<span data-ttu-id="8a763-106">Test-AzContainerRegistryNameAvailability cmdlet 'i, kapsayıcı kayıt defteri adının geçerli ve kullanılabilir olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="8a763-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="8a763-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a763-107">EXAMPLES</span></span>

### <span data-ttu-id="8a763-108">Örnek 1: kapsayıcı kayıt defteri adının uygunluk durumunu denetler</span><span class="sxs-lookup"><span data-stu-id="8a763-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="8a763-109">Bu komut, SomeRegistryName kapsayıcısı kayıt defteri adının kullanılabilirliğini denetler \` \` .</span><span class="sxs-lookup"><span data-stu-id="8a763-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="8a763-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a763-110">PARAMETERS</span></span>

### <span data-ttu-id="8a763-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a763-111">-DefaultProfile</span></span>
<span data-ttu-id="8a763-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8a763-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a763-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a763-113">-Name</span></span>
<span data-ttu-id="8a763-114">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="8a763-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="8a763-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a763-115">CommonParameters</span></span>
<span data-ttu-id="8a763-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a763-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a763-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a763-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a763-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a763-118">INPUTS</span></span>

### <span data-ttu-id="8a763-119">System. String</span><span class="sxs-lookup"><span data-stu-id="8a763-119">System.String</span></span>

## <span data-ttu-id="8a763-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a763-120">OUTPUTS</span></span>

### <span data-ttu-id="8a763-121">Microsoft. Azure. Management. ContainerRegistry. modeller. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="8a763-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="8a763-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a763-122">NOTES</span></span>

## <span data-ttu-id="8a763-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a763-123">RELATED LINKS</span></span>

[<span data-ttu-id="8a763-124">Yeni-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8a763-124">New-AzContainerRegistry</span></span>]()

