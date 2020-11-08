---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095927"
---
# <span data-ttu-id="4877c-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="4877c-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="4877c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4877c-102">SYNOPSIS</span></span>
<span data-ttu-id="4877c-103">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="4877c-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="4877c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4877c-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4877c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4877c-105">DESCRIPTION</span></span>
<span data-ttu-id="4877c-106">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="4877c-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="4877c-107">Tüm anahtarlar için ConnectionString veya belirli bir anahtar adına göre filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4877c-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="4877c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4877c-108">EXAMPLES</span></span>

### <span data-ttu-id="4877c-109">Örnek 1 tüm IotHub ConnectionString Ifadesini al</span><span class="sxs-lookup"><span data-stu-id="4877c-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4877c-110">"Myiothub" adındaki iothub tüm anahtarlarının ConnectionString 'i alır</span><span class="sxs-lookup"><span data-stu-id="4877c-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="4877c-111">Örnek 2 belirli bir anahtarın IotHub ConnectionString Ifadesini alma</span><span class="sxs-lookup"><span data-stu-id="4877c-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="4877c-112">"Myiothub" adlı iothub "myKey" adlı anahtarın ConnectionString öğesini alır</span><span class="sxs-lookup"><span data-stu-id="4877c-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="4877c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4877c-113">PARAMETERS</span></span>

### <span data-ttu-id="4877c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4877c-114">-DefaultProfile</span></span>
<span data-ttu-id="4877c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4877c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4877c-116">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="4877c-116">-KeyName</span></span>
<span data-ttu-id="4877c-117">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="4877c-117">Name of the Key</span></span>

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

### <span data-ttu-id="4877c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="4877c-118">-Name</span></span>
<span data-ttu-id="4877c-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="4877c-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="4877c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4877c-120">-ResourceGroupName</span></span>
<span data-ttu-id="4877c-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4877c-121">Resource Group Name</span></span>

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

### <span data-ttu-id="4877c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4877c-122">CommonParameters</span></span>
<span data-ttu-id="4877c-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4877c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4877c-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4877c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4877c-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4877c-125">INPUTS</span></span>

### <span data-ttu-id="4877c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4877c-126">System.String</span></span>

## <span data-ttu-id="4877c-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4877c-127">OUTPUTS</span></span>

### <span data-ttu-id="4877c-128">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="4877c-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="4877c-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4877c-129">NOTES</span></span>

## <span data-ttu-id="4877c-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4877c-130">RELATED LINKS</span></span>
