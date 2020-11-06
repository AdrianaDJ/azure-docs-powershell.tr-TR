---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: db2cf6c9daae5b96642a6408b990276feffc8598
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593114"
---
# <span data-ttu-id="05deb-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="05deb-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="05deb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05deb-102">SYNOPSIS</span></span>
<span data-ttu-id="05deb-103">Bir IotHub anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="05deb-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05deb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05deb-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05deb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="05deb-105">DESCRIPTION</span></span>
<span data-ttu-id="05deb-106">Bir IotHub anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="05deb-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="05deb-107">Tüm anahtarları listeleyebilir veya listeyi belirli bir anahtar adına göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05deb-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="05deb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05deb-108">EXAMPLES</span></span>

### <span data-ttu-id="05deb-109">Örnek 1 tüm tuşları al</span><span class="sxs-lookup"><span data-stu-id="05deb-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="05deb-110">"Myiothub" adındaki IotHub için tüm tuşları alır</span><span class="sxs-lookup"><span data-stu-id="05deb-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="05deb-111">Örnek 2 belirli bir anahtarla ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="05deb-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="05deb-112">"Myiothub" adlı IotHub "ıothubowner" adlı bir anahtarın bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="05deb-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="05deb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05deb-113">PARAMETERS</span></span>

### <span data-ttu-id="05deb-114">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="05deb-114">-KeyName</span></span>
<span data-ttu-id="05deb-115">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="05deb-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05deb-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="05deb-116">-Name</span></span>
<span data-ttu-id="05deb-117">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="05deb-117">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05deb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05deb-118">-ResourceGroupName</span></span>
<span data-ttu-id="05deb-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="05deb-119">Resource Group Name</span></span>

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

### <span data-ttu-id="05deb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05deb-120">-DefaultProfile</span></span>
<span data-ttu-id="05deb-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05deb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05deb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05deb-122">CommonParameters</span></span>
<span data-ttu-id="05deb-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05deb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05deb-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05deb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05deb-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05deb-125">INPUTS</span></span>

### <span data-ttu-id="05deb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="05deb-126">System.String</span></span>

## <span data-ttu-id="05deb-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05deb-127">OUTPUTS</span></span>

### <span data-ttu-id="05deb-128">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="05deb-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="05deb-129">System. Koleksiyonlar. Generic. LIST \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstif, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="05deb-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="05deb-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05deb-130">NOTES</span></span>

## <span data-ttu-id="05deb-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05deb-131">RELATED LINKS</span></span>

