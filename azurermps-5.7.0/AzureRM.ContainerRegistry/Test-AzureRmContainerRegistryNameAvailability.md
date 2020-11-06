---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: da415c21532ea0b2178cc2a75d6a3d09bdc2d50b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591031"
---
# <span data-ttu-id="46525-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="46525-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="46525-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46525-102">SYNOPSIS</span></span>
<span data-ttu-id="46525-103">Kapsayıcı kayıt defteri adının kullanılabilirliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="46525-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46525-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46525-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46525-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46525-105">DESCRIPTION</span></span>
<span data-ttu-id="46525-106">Test-AzureRmContainerRegistryNameAvailability cmdlet 'i, kapsayıcı kayıt defteri adının geçerli ve kullanılabilir olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="46525-106">The Test-AzureRmContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="46525-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46525-107">EXAMPLES</span></span>

### <span data-ttu-id="46525-108">Örnek 1: kapsayıcı kayıt defteri adının uygunluk durumunu denetler</span><span class="sxs-lookup"><span data-stu-id="46525-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="46525-109">Bu komut, SomeRegistryName kapsayıcısı kayıt defteri adının kullanılabilirliğini denetler \` \` .</span><span class="sxs-lookup"><span data-stu-id="46525-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="46525-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46525-110">PARAMETERS</span></span>

### <span data-ttu-id="46525-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="46525-111">-Name</span></span>
<span data-ttu-id="46525-112">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="46525-112">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46525-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46525-113">-DefaultProfile</span></span>
<span data-ttu-id="46525-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="46525-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46525-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46525-115">CommonParameters</span></span>
<span data-ttu-id="46525-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46525-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46525-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46525-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46525-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46525-118">INPUTS</span></span>

### <span data-ttu-id="46525-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="46525-119">None</span></span>
<span data-ttu-id="46525-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="46525-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46525-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46525-121">OUTPUTS</span></span>

### <span data-ttu-id="46525-122">Microsoft. Azure. Management. ContainerRegistry. modeller. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="46525-122">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="46525-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46525-123">NOTES</span></span>

## <span data-ttu-id="46525-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46525-124">RELATED LINKS</span></span>

[<span data-ttu-id="46525-125">Yeni-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="46525-125">New-AzureRmContainerRegistry</span></span>]()

