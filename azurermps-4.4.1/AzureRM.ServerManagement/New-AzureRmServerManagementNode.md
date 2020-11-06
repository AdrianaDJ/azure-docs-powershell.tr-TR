---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: e77059b94f9311caf25b58f2d626f0cafc4657e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590635"
---
# <span data-ttu-id="611af-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="611af-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="611af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="611af-102">SYNOPSIS</span></span>
<span data-ttu-id="611af-103">Sunucu yönetimi düğümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="611af-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="611af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="611af-104">SYNTAX</span></span>

### <span data-ttu-id="611af-105">ByName</span><span class="sxs-lookup"><span data-stu-id="611af-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="611af-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="611af-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="611af-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="611af-107">DESCRIPTION</span></span>
<span data-ttu-id="611af-108">**Yeni-AzureRmServerManagementNode** cmdlet 'ı bir Azure Server Yönetim düğümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="611af-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="611af-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="611af-109">EXAMPLES</span></span>

## <span data-ttu-id="611af-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="611af-110">PARAMETERS</span></span>

### <span data-ttu-id="611af-111">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="611af-111">-ComputerName</span></span>
<span data-ttu-id="611af-112">Yönetilmekte olan bilgisayarın bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="611af-112">Specifies the computer name of the computer that is being managed.</span></span>

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

### <span data-ttu-id="611af-113">-Credential</span><span class="sxs-lookup"><span data-stu-id="611af-113">-Credential</span></span>
<span data-ttu-id="611af-114">Sunucu Yönetimi düğümüne bağlantı için bir **PSCredential** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="611af-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="611af-115">Kimlik bilgisi nesnesi edinmek için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="611af-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="611af-116">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="611af-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611af-117">-Ağ Geçidi</span><span class="sxs-lookup"><span data-stu-id="611af-117">-Gateway</span></span>
<span data-ttu-id="611af-118">Düğümü yöneten ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="611af-118">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="611af-119">Bu parametre, *Resourcegroupname* , *GatewayName* ve *Location* parametreleri yerine kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="611af-119">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="611af-120">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="611af-120">-GatewayName</span></span>
<span data-ttu-id="611af-121">Düğüme erişen ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="611af-121">Specifies the name of the gateway that accesses the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="611af-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="611af-122">-Location</span></span>
<span data-ttu-id="611af-123">Bu cmdlet 'in düğümü oluşturduğu konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="611af-123">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="611af-124">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="611af-124">-NodeName</span></span>
<span data-ttu-id="611af-125">Düğümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="611af-125">Specifies the name of the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="611af-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="611af-126">-ResourceGroupName</span></span>
<span data-ttu-id="611af-127">Bu cmdlet 'in düğümü oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="611af-127">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

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

### <span data-ttu-id="611af-128">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="611af-128">-Tags</span></span>
<span data-ttu-id="611af-129">Etiketleri anahtar-değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="611af-129">Specifies tags as key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="611af-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="611af-130">-DefaultProfile</span></span>
<span data-ttu-id="611af-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="611af-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="611af-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611af-132">CommonParameters</span></span>
<span data-ttu-id="611af-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="611af-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611af-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="611af-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611af-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="611af-135">INPUTS</span></span>

### <span data-ttu-id="611af-136">Geçidi</span><span class="sxs-lookup"><span data-stu-id="611af-136">Gateway</span></span>
<span data-ttu-id="611af-137">' Ağ Geçidi ' parametresi ardışık düzenin ' Gateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="611af-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="611af-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="611af-138">OUTPUTS</span></span>

### <span data-ttu-id="611af-139">Microsoft. Azure. Commands. ServerManagement. model. Node</span><span class="sxs-lookup"><span data-stu-id="611af-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="611af-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="611af-140">NOTES</span></span>

## <span data-ttu-id="611af-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="611af-141">RELATED LINKS</span></span>

[<span data-ttu-id="611af-142">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="611af-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="611af-143">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="611af-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


