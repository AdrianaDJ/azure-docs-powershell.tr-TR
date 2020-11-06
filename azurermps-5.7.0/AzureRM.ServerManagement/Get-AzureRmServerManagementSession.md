---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8942D757-B204-49CE-BCDE-68C3722913B3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
ms.openlocfilehash: e32f9268309562b45e13df164631e18d28cceb0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588781"
---
# <span data-ttu-id="8e8e6-101">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="8e8e6-101">Get-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="8e8e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="8e8e6-103">Sunucu Yönetimi oturumu alır.</span><span class="sxs-lookup"><span data-stu-id="8e8e6-103">Gets a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e8e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e8e6-104">SYNTAX</span></span>

### <span data-ttu-id="8e8e6-105">Bydüğümadı</span><span class="sxs-lookup"><span data-stu-id="8e8e6-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e8e6-106">BySession</span><span class="sxs-lookup"><span data-stu-id="8e8e6-106">BySession</span></span>
```
Get-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e8e6-107">ByNode</span><span class="sxs-lookup"><span data-stu-id="8e8e6-107">ByNode</span></span>
```
Get-AzureRmServerManagementSession [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e8e6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e8e6-108">DESCRIPTION</span></span>
<span data-ttu-id="8e8e6-109">**Get-AzureRmServerManagementSession** cmdlet 'i tek bir Azure Server yönetim oturumu alır.</span><span class="sxs-lookup"><span data-stu-id="8e8e6-109">The **Get-AzureRmServerManagementSession** cmdlet gets a single Azure Server Management session.</span></span>

## <span data-ttu-id="8e8e6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e8e6-110">EXAMPLES</span></span>

## <span data-ttu-id="8e8e6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e8e6-111">PARAMETERS</span></span>

### <span data-ttu-id="8e8e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e8e6-112">-DefaultProfile</span></span>
<span data-ttu-id="8e8e6-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e8e6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e8e6-114">-Node</span><span class="sxs-lookup"><span data-stu-id="8e8e6-114">-Node</span></span>
<span data-ttu-id="8e8e6-115">*Resourcegroupname* ve *DüğümAdı* parametrelerini almak için kullanılan var olan bir **node** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e8e6-115">Specifies an existing **Node** object that is used to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>
<span data-ttu-id="8e8e6-116">*Oturumadı* parametresi için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8e8e6-116">You must also specify a value for the *SessionName* parameter.</span></span>

```yaml
Type: Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8e6-117">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="8e8e6-117">-NodeName</span></span>
<span data-ttu-id="8e8e6-118">Oturumun bulunduğu düğümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e8e6-118">Specifies the name of the node where the session is located.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8e6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e8e6-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e8e6-120">Bu cmdlet 'in oturumu geri alma aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e8e6-120">Specifies the name of the resource group for which this cmdlet gets the retrieve the session.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8e6-121">-Oturum</span><span class="sxs-lookup"><span data-stu-id="8e8e6-121">-Session</span></span>
<span data-ttu-id="8e8e6-122">*Resourcegroupname* , *DüğümAdı* ve *oturumadı* parametrelerini almak için kullanılan bir **oturum** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e8e6-122">Specifies an existing **Session** object that is used to get the *ResourceGroupName* , the *NodeName* , and the *SessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8e6-123">-OturumAdı</span><span class="sxs-lookup"><span data-stu-id="8e8e6-123">-SessionName</span></span>
<span data-ttu-id="8e8e6-124">Bu cmdlet 'in aldığı oturumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e8e6-124">Specifies the name of the session in which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySession
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e8e6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e8e6-125">CommonParameters</span></span>
<span data-ttu-id="8e8e6-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e8e6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e8e6-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e8e6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e8e6-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e8e6-128">INPUTS</span></span>

### <span data-ttu-id="8e8e6-129">Düğümü</span><span class="sxs-lookup"><span data-stu-id="8e8e6-129">Node</span></span>
<span data-ttu-id="8e8e6-130">' Node ' parametresi ardışık düzenin ' node ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8e8e6-130">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

### <span data-ttu-id="8e8e6-131">Oturumu</span><span class="sxs-lookup"><span data-stu-id="8e8e6-131">Session</span></span>
<span data-ttu-id="8e8e6-132">Parametre ' Session ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="8e8e6-132">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="8e8e6-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e8e6-133">OUTPUTS</span></span>

### <span data-ttu-id="8e8e6-134">Microsoft. Azure. Commands. ServerManagement. model. Session</span><span class="sxs-lookup"><span data-stu-id="8e8e6-134">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="8e8e6-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e8e6-135">NOTES</span></span>

## <span data-ttu-id="8e8e6-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e8e6-136">RELATED LINKS</span></span>

[<span data-ttu-id="8e8e6-137">Azure Server Yönetim cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="8e8e6-137">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


