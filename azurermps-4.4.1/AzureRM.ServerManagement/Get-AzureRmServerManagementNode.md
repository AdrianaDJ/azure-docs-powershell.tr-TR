---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 4EE30890-B09B-4811-88AD-4BF4FD47E431
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
ms.openlocfilehash: ab49458426b7035a20e63ca62d86124d79291b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590649"
---
# <span data-ttu-id="24f1c-101">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="24f1c-101">Get-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="24f1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="24f1c-103">Bir veya daha fazla sunucu yönetimi düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="24f1c-103">Gets one or more Server Management nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24f1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24f1c-104">SYNTAX</span></span>

### <span data-ttu-id="24f1c-105">Bydüğümadı</span><span class="sxs-lookup"><span data-stu-id="24f1c-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementNode [[-ResourceGroupName] <String>] [[-NodeName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24f1c-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="24f1c-106">ByNode</span></span>
```
Get-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24f1c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="24f1c-107">DESCRIPTION</span></span>
<span data-ttu-id="24f1c-108">**Get-AzureRmServerManagementNode** cmdlet 'i bir veya daha fazla Azure Server yönetim düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="24f1c-108">The **Get-AzureRmServerManagementNode** cmdlet gets one or more Azure Server Management nodes.</span></span>

## <span data-ttu-id="24f1c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24f1c-109">EXAMPLES</span></span>

## <span data-ttu-id="24f1c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24f1c-110">PARAMETERS</span></span>

### <span data-ttu-id="24f1c-111">-Node</span><span class="sxs-lookup"><span data-stu-id="24f1c-111">-Node</span></span>
<span data-ttu-id="24f1c-112">*Resourcegroupname* ve *DüğümAdı* parametrelerinin alınacağı varolan bir düğümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="24f1c-112">Specifies an existing node from which to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24f1c-113">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="24f1c-113">-NodeName</span></span>
<span data-ttu-id="24f1c-114">Bu cmdlet 'in aldığı düğümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24f1c-114">Specifies the name of the node for which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f1c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f1c-115">-ResourceGroupName</span></span>
<span data-ttu-id="24f1c-116">Düğümlerin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24f1c-116">Specifies the name of the resource group in which the nodes belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f1c-117">-DefaultProfile</span></span>
<span data-ttu-id="24f1c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24f1c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24f1c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f1c-119">CommonParameters</span></span>
<span data-ttu-id="24f1c-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24f1c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f1c-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24f1c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f1c-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24f1c-122">INPUTS</span></span>

### <span data-ttu-id="24f1c-123">Düğümü</span><span class="sxs-lookup"><span data-stu-id="24f1c-123">Node</span></span>
<span data-ttu-id="24f1c-124">' Node ' parametresi ardışık düzenin ' node ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="24f1c-124">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="24f1c-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24f1c-125">OUTPUTS</span></span>

### <span data-ttu-id="24f1c-126">Microsoft. Azure. Commands. ServerManagement. model. Node</span><span class="sxs-lookup"><span data-stu-id="24f1c-126">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="24f1c-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24f1c-127">NOTES</span></span>

## <span data-ttu-id="24f1c-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24f1c-128">RELATED LINKS</span></span>

[<span data-ttu-id="24f1c-129">Yeni-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="24f1c-129">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)

[<span data-ttu-id="24f1c-130">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="24f1c-130">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


