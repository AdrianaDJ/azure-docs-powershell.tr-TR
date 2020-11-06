---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: 498be36141d1a44d33cdcb351b92d5b6908071c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573273"
---
# <span data-ttu-id="a1b72-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="a1b72-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="a1b72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1b72-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b72-103">Sunucu yönetimi düğümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1b72-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1b72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1b72-104">SYNTAX</span></span>

### <span data-ttu-id="a1b72-105">ByName</span><span class="sxs-lookup"><span data-stu-id="a1b72-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1b72-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="a1b72-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1b72-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1b72-107">DESCRIPTION</span></span>
<span data-ttu-id="a1b72-108">**Yeni-AzureRmServerManagementNode** cmdlet 'ı bir Azure Server Yönetim düğümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1b72-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="a1b72-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1b72-109">EXAMPLES</span></span>

## <span data-ttu-id="a1b72-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1b72-110">PARAMETERS</span></span>

### <span data-ttu-id="a1b72-111">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="a1b72-111">-ComputerName</span></span>
<span data-ttu-id="a1b72-112">Yönetilmekte olan bilgisayarın bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1b72-112">Specifies the computer name of the computer that is being managed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b72-113">-Credential</span><span class="sxs-lookup"><span data-stu-id="a1b72-113">-Credential</span></span>
<span data-ttu-id="a1b72-114">Sunucu Yönetimi düğümüne bağlantı için bir **PSCredential** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1b72-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="a1b72-115">Kimlik bilgisi nesnesi edinmek için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a1b72-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="a1b72-116">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a1b72-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b72-117">-DefaultProfile</span></span>
<span data-ttu-id="a1b72-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1b72-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b72-119">-Ağ Geçidi</span><span class="sxs-lookup"><span data-stu-id="a1b72-119">-Gateway</span></span>
<span data-ttu-id="a1b72-120">Düğümü yöneten ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1b72-120">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="a1b72-121">Bu parametre, *Resourcegroupname* , *GatewayName* ve *Location* parametreleri yerine kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a1b72-121">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b72-122">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="a1b72-122">-GatewayName</span></span>
<span data-ttu-id="a1b72-123">Düğüme erişen ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1b72-123">Specifies the name of the gateway that accesses the node.</span></span>

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

### <span data-ttu-id="a1b72-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="a1b72-124">-Location</span></span>
<span data-ttu-id="a1b72-125">Bu cmdlet 'in düğümü oluşturduğu konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1b72-125">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b72-126">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="a1b72-126">-NodeName</span></span>
<span data-ttu-id="a1b72-127">Düğümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1b72-127">Specifies the name of the node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b72-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b72-128">-ResourceGroupName</span></span>
<span data-ttu-id="a1b72-129">Bu cmdlet 'in düğümü oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1b72-129">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

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

### <span data-ttu-id="a1b72-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a1b72-130">-Tag</span></span>
<span data-ttu-id="a1b72-131">Nesneyle ilişkilendirilmiş anahtar/değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="a1b72-131">Key/value pairs associated with the object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b72-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b72-132">CommonParameters</span></span>
<span data-ttu-id="a1b72-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1b72-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b72-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b72-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b72-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1b72-135">INPUTS</span></span>

### <span data-ttu-id="a1b72-136">Geçidi</span><span class="sxs-lookup"><span data-stu-id="a1b72-136">Gateway</span></span>
<span data-ttu-id="a1b72-137">' Ağ Geçidi ' parametresi ardışık düzenin ' Gateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a1b72-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="a1b72-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1b72-138">OUTPUTS</span></span>

### <span data-ttu-id="a1b72-139">Microsoft. Azure. Commands. ServerManagement. model. Node</span><span class="sxs-lookup"><span data-stu-id="a1b72-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="a1b72-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1b72-140">NOTES</span></span>

## <span data-ttu-id="a1b72-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1b72-141">RELATED LINKS</span></span>

[<span data-ttu-id="a1b72-142">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="a1b72-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="a1b72-143">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="a1b72-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


