---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 78fa17dee687547b617ff02dd11ecbf662e48040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762140"
---
# <span data-ttu-id="bbdde-101">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="bbdde-101">Remove-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="bbdde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbdde-102">SYNOPSIS</span></span>
<span data-ttu-id="bbdde-103">Sunucu Yönetimi düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bbdde-103">Removes a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbdde-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbdde-104">SYNTAX</span></span>

### <span data-ttu-id="bbdde-105">ByName</span><span class="sxs-lookup"><span data-stu-id="bbdde-105">ByName</span></span>
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbdde-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="bbdde-106">ByObject</span></span>
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbdde-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbdde-107">DESCRIPTION</span></span>
<span data-ttu-id="bbdde-108">**Remove-AzureRmServerManagementNode** cmdlet 'ı bir Azure Server yönetim düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bbdde-108">The **Remove-AzureRmServerManagementNode** cmdlet removes an Azure Server Management node.</span></span>

## <span data-ttu-id="bbdde-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbdde-109">EXAMPLES</span></span>

## <span data-ttu-id="bbdde-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbdde-110">PARAMETERS</span></span>

### <span data-ttu-id="bbdde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbdde-111">-DefaultProfile</span></span>
<span data-ttu-id="bbdde-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbdde-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbdde-113">-Node</span><span class="sxs-lookup"><span data-stu-id="bbdde-113">-Node</span></span>
<span data-ttu-id="bbdde-114">Bu cmdlet 'in kaldırıldığı düğümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbdde-114">Specifies the node for which this cmdlet removes.</span></span>

<span data-ttu-id="bbdde-115">Bu parametre, *Resourcegroupname* ve *DüğümAdı* parametrelerinin yerine kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bbdde-115">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdde-116">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="bbdde-116">-NodeName</span></span>
<span data-ttu-id="bbdde-117">Bu cmdlet 'in kaldırıldığı düğümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbdde-117">Specifies the name of the node for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdde-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbdde-118">-ResourceGroupName</span></span>
<span data-ttu-id="bbdde-119">Düğümün ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbdde-119">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdde-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbdde-120">CommonParameters</span></span>
<span data-ttu-id="bbdde-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbdde-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbdde-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbdde-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbdde-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbdde-123">INPUTS</span></span>

### <span data-ttu-id="bbdde-124">Düğümü</span><span class="sxs-lookup"><span data-stu-id="bbdde-124">Node</span></span>
<span data-ttu-id="bbdde-125">' Node ' parametresi ardışık düzenin ' node ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bbdde-125">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="bbdde-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbdde-126">OUTPUTS</span></span>

## <span data-ttu-id="bbdde-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbdde-127">NOTES</span></span>

## <span data-ttu-id="bbdde-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbdde-128">RELATED LINKS</span></span>

[<span data-ttu-id="bbdde-129">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="bbdde-129">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="bbdde-130">Yeni-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="bbdde-130">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)


