---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: 6e56bab4fb17aa485a1103a2be3a8b5592fc4393
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594033"
---
# <span data-ttu-id="c0504-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="c0504-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="c0504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0504-102">SYNOPSIS</span></span>
<span data-ttu-id="c0504-103">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="c0504-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0504-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0504-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0504-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0504-105">DESCRIPTION</span></span>
<span data-ttu-id="c0504-106">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="c0504-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="c0504-107">Tüm anahtarlar için ConnectionString veya belirli bir anahtar adına göre filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0504-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="c0504-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0504-108">EXAMPLES</span></span>

### <span data-ttu-id="c0504-109">Örnek 1 tüm IotHub ConnectionString Ifadesini al</span><span class="sxs-lookup"><span data-stu-id="c0504-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c0504-110">"Myiothub" adındaki iothub tüm anahtarlarının ConnectionString 'i alır</span><span class="sxs-lookup"><span data-stu-id="c0504-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="c0504-111">Örnek 2 belirli bir anahtarın IotHub ConnectionString Ifadesini alma</span><span class="sxs-lookup"><span data-stu-id="c0504-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="c0504-112">"Myiothub" adlı iothub "myKey" adlı anahtarın ConnectionString öğesini alır</span><span class="sxs-lookup"><span data-stu-id="c0504-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="c0504-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0504-113">PARAMETERS</span></span>

### <span data-ttu-id="c0504-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0504-114">-DefaultProfile</span></span>
<span data-ttu-id="c0504-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c0504-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0504-116">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="c0504-116">-KeyName</span></span>
<span data-ttu-id="c0504-117">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="c0504-117">Name of the Key</span></span>

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

### <span data-ttu-id="c0504-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0504-118">-Name</span></span>
<span data-ttu-id="c0504-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="c0504-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="c0504-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0504-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0504-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c0504-121">Resource Group Name</span></span>

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

### <span data-ttu-id="c0504-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0504-122">CommonParameters</span></span>
<span data-ttu-id="c0504-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0504-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0504-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0504-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0504-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0504-125">INPUTS</span></span>

### <span data-ttu-id="c0504-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c0504-126">System.String</span></span>

## <span data-ttu-id="c0504-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0504-127">OUTPUTS</span></span>

### <span data-ttu-id="c0504-128">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="c0504-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="c0504-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0504-129">NOTES</span></span>

## <span data-ttu-id="c0504-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0504-130">RELATED LINKS</span></span>
