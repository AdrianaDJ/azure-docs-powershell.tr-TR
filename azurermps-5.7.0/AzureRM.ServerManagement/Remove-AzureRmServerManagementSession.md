---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: b2ebde9e6cf0e94e43d41cd75ee7ee09674fc3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592896"
---
# <span data-ttu-id="2cca2-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="2cca2-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="2cca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cca2-102">SYNOPSIS</span></span>
<span data-ttu-id="2cca2-103">Sunucu yönetimi oturumunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2cca2-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cca2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2cca2-104">SYNTAX</span></span>

### <span data-ttu-id="2cca2-105">ByName</span><span class="sxs-lookup"><span data-stu-id="2cca2-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cca2-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="2cca2-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cca2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2cca2-107">DESCRIPTION</span></span>
<span data-ttu-id="2cca2-108">**Remove-AzureRmServerManagementSession** cmdlet 'ı bir Azure Server Yönetim oturumunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2cca2-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="2cca2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2cca2-109">EXAMPLES</span></span>

## <span data-ttu-id="2cca2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2cca2-110">PARAMETERS</span></span>

### <span data-ttu-id="2cca2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cca2-111">-DefaultProfile</span></span>
<span data-ttu-id="2cca2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2cca2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cca2-113">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="2cca2-113">-NodeName</span></span>
<span data-ttu-id="2cca2-114">Bu cmdlet 'in oturumu kaldırdığı düğümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cca2-114">Specifies the name of the node on which this cmdlet removes the session.</span></span>

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

### <span data-ttu-id="2cca2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cca2-115">-ResourceGroupName</span></span>
<span data-ttu-id="2cca2-116">Oturumun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cca2-116">Specifies the name of the resource group that the session belongs to.</span></span>

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

### <span data-ttu-id="2cca2-117">-Oturum</span><span class="sxs-lookup"><span data-stu-id="2cca2-117">-Session</span></span>
<span data-ttu-id="2cca2-118">Bu cmdlet 'in kaldırıldığı oturumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cca2-118">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="2cca2-119">Bu parametre, *Resourcegroupname* , *düğügroupname* ve *oturumadı* parametreleri yerine kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2cca2-119">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cca2-120">-OturumAdı</span><span class="sxs-lookup"><span data-stu-id="2cca2-120">-SessionName</span></span>
<span data-ttu-id="2cca2-121">Bu cmdlet 'in kaldırıldığı oturumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cca2-121">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cca2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cca2-122">CommonParameters</span></span>
<span data-ttu-id="2cca2-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2cca2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cca2-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cca2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cca2-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2cca2-125">INPUTS</span></span>

### <span data-ttu-id="2cca2-126">Oturumu</span><span class="sxs-lookup"><span data-stu-id="2cca2-126">Session</span></span>
<span data-ttu-id="2cca2-127">Parametre ' Session ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="2cca2-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="2cca2-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2cca2-128">OUTPUTS</span></span>

## <span data-ttu-id="2cca2-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2cca2-129">NOTES</span></span>

## <span data-ttu-id="2cca2-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2cca2-130">RELATED LINKS</span></span>

[<span data-ttu-id="2cca2-131">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="2cca2-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="2cca2-132">Yeni-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="2cca2-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)


