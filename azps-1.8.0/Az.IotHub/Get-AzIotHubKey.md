---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: ac56d5392025a85d0310862a1786dde3d0f8ca2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916471"
---
# <span data-ttu-id="55ebb-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="55ebb-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="55ebb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="55ebb-103">Bir IotHub anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="55ebb-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="55ebb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55ebb-104">SYNTAX</span></span>

```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55ebb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55ebb-105">DESCRIPTION</span></span>
<span data-ttu-id="55ebb-106">Bir IotHub anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="55ebb-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="55ebb-107">Tüm anahtarları listeleyebilir veya listeyi belirli bir anahtar adına göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="55ebb-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="55ebb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55ebb-108">EXAMPLES</span></span>

### <span data-ttu-id="55ebb-109">Örnek 1 tüm tuşları al</span><span class="sxs-lookup"><span data-stu-id="55ebb-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="55ebb-110">"Myiothub" adındaki IotHub için tüm tuşları alır</span><span class="sxs-lookup"><span data-stu-id="55ebb-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="55ebb-111">Örnek 2 belirli bir anahtarla ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="55ebb-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="55ebb-112">"Myiothub" adlı IotHub "ıothubowner" adlı bir anahtarın bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="55ebb-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="55ebb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55ebb-113">PARAMETERS</span></span>

### <span data-ttu-id="55ebb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ebb-114">-DefaultProfile</span></span>
<span data-ttu-id="55ebb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="55ebb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ebb-116">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="55ebb-116">-KeyName</span></span>
<span data-ttu-id="55ebb-117">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="55ebb-117">Name of the Key</span></span>

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

### <span data-ttu-id="55ebb-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="55ebb-118">-Name</span></span>
<span data-ttu-id="55ebb-119">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="55ebb-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="55ebb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ebb-120">-ResourceGroupName</span></span>
<span data-ttu-id="55ebb-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="55ebb-121">Resource Group Name</span></span>

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

### <span data-ttu-id="55ebb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ebb-122">CommonParameters</span></span>
<span data-ttu-id="55ebb-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55ebb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ebb-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55ebb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ebb-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55ebb-125">INPUTS</span></span>

### <span data-ttu-id="55ebb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="55ebb-126">System.String</span></span>

## <span data-ttu-id="55ebb-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55ebb-127">OUTPUTS</span></span>

### <span data-ttu-id="55ebb-128">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="55ebb-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="55ebb-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55ebb-129">NOTES</span></span>

## <span data-ttu-id="55ebb-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55ebb-130">RELATED LINKS</span></span>
