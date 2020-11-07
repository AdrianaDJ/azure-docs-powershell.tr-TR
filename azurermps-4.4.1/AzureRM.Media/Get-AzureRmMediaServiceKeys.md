---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 6cef357b636a48e433d545a56d2b5105556842da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764815"
---
# <span data-ttu-id="f3f8b-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="f3f8b-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="f3f8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f8b-103">Medya hizmetiyle ilişkili REST uç noktasına erişmek için önemli bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3f8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3f8b-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3f8b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="f3f8b-106">**Get-AzureRmMediaServiceKeys** cmdlet 'i Azure Medya hizmeti Ile Ilişkili Representational State Transfer (REST) uç noktasına erişmek için temel bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="f3f8b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3f8b-107">EXAMPLES</span></span>

### <span data-ttu-id="f3f8b-108">Örnek 1: medya hizmetine erişim için temel bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="f3f8b-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="f3f8b-109">Bu komut, ResourceGroup001 adındaki kaynak grubuna ait MediaService001 adındaki medya hizmetine erişmeye yönelik anahtar bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="f3f8b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3f8b-110">PARAMETERS</span></span>

### <span data-ttu-id="f3f8b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f3f8b-111">-AccountName</span></span>
<span data-ttu-id="f3f8b-112">Bu cmdlet 'in medya hizmeti anahtarlarını aldığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f8b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3f8b-113">-ResourceGroupName</span></span>
<span data-ttu-id="f3f8b-114">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-114">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f8b-115">-DefaultProfile</span></span>
<span data-ttu-id="f3f8b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3f8b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f8b-117">CommonParameters</span></span>
<span data-ttu-id="f3f8b-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f8b-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f8b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f8b-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3f8b-120">INPUTS</span></span>

## <span data-ttu-id="f3f8b-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3f8b-121">OUTPUTS</span></span>

### <span data-ttu-id="f3f8b-122">Microsoft. Azure. Commands. Media. modeller. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="f3f8b-122">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="f3f8b-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3f8b-123">NOTES</span></span>

## <span data-ttu-id="f3f8b-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3f8b-124">RELATED LINKS</span></span>

[<span data-ttu-id="f3f8b-125">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="f3f8b-125">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


