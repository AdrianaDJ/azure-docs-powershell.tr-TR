---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 0ae3e221ee39a00381f009f45a9a2f508a552b6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589118"
---
# <span data-ttu-id="34e7d-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="34e7d-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="34e7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="34e7d-103">Sunucu Yönetimi oturumu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34e7d-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34e7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34e7d-104">SYNTAX</span></span>

### <span data-ttu-id="34e7d-105">ByName</span><span class="sxs-lookup"><span data-stu-id="34e7d-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34e7d-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="34e7d-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34e7d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="34e7d-107">DESCRIPTION</span></span>
<span data-ttu-id="34e7d-108">**Yeni-AzureRmServerManagementSession** cmdlet 'ı bir Azure Server yönetim oturumu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34e7d-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="34e7d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34e7d-109">EXAMPLES</span></span>

## <span data-ttu-id="34e7d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34e7d-110">PARAMETERS</span></span>

### <span data-ttu-id="34e7d-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="34e7d-111">-Credential</span></span>
<span data-ttu-id="34e7d-112">Sunucu yönetimi oturumuna bağlantı için bir **PSCredential** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="34e7d-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="34e7d-113">Kimlik bilgisi nesnesi edinmek için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="34e7d-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="34e7d-114">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="34e7d-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e7d-115">-Node</span><span class="sxs-lookup"><span data-stu-id="34e7d-115">-Node</span></span>
<span data-ttu-id="34e7d-116">Bu cmdlet 'in oturum oluşturduğu düğümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="34e7d-116">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="34e7d-117">Bu parametre, *Resourcegroupname* ve *DüğümAdı* parametrelerinin yerine kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="34e7d-117">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

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

### <span data-ttu-id="34e7d-118">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="34e7d-118">-NodeName</span></span>
<span data-ttu-id="34e7d-119">Bu cmdlet 'in oturum oluşturduğu düğümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34e7d-119">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e7d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e7d-120">-ResourceGroupName</span></span>
<span data-ttu-id="34e7d-121">Bu cmdlet 'in oturum oluşturduğu düğümün kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="34e7d-121">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e7d-122">-OturumAdı</span><span class="sxs-lookup"><span data-stu-id="34e7d-122">-SessionName</span></span>
<span data-ttu-id="34e7d-123">Oturum için kullanılacak adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="34e7d-123">Specifies the name to use for the session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e7d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e7d-124">-DefaultProfile</span></span>
<span data-ttu-id="34e7d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34e7d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34e7d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e7d-126">CommonParameters</span></span>
<span data-ttu-id="34e7d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34e7d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e7d-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e7d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e7d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34e7d-129">INPUTS</span></span>

### <span data-ttu-id="34e7d-130">Düğümü</span><span class="sxs-lookup"><span data-stu-id="34e7d-130">Node</span></span>
<span data-ttu-id="34e7d-131">' Node ' parametresi ardışık düzenin ' node ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="34e7d-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="34e7d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34e7d-132">OUTPUTS</span></span>

### <span data-ttu-id="34e7d-133">Microsoft. Azure. Commands. ServerManagement. model. Session</span><span class="sxs-lookup"><span data-stu-id="34e7d-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="34e7d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34e7d-134">NOTES</span></span>

## <span data-ttu-id="34e7d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34e7d-135">RELATED LINKS</span></span>

