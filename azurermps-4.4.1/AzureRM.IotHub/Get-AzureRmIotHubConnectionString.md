---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: 52c5bee4e699ff063794f140ce4360669180a164
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763727"
---
# <span data-ttu-id="4c4b7-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="4c4b7-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="4c4b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="4c4b7-103">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="4c4b7-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c4b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c4b7-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c4b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c4b7-105">DESCRIPTION</span></span>
<span data-ttu-id="4c4b7-106">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="4c4b7-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="4c4b7-107">Tüm anahtarlar için ConnectionString veya belirli bir anahtar adına göre filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c4b7-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="4c4b7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c4b7-108">EXAMPLES</span></span>

### <span data-ttu-id="4c4b7-109">Örnek 1 tüm IotHub ConnectionString Ifadesini al</span><span class="sxs-lookup"><span data-stu-id="4c4b7-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4c4b7-110">"Myiothub" adındaki iothub tüm anahtarlarının ConnectionString 'i alır</span><span class="sxs-lookup"><span data-stu-id="4c4b7-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="4c4b7-111">Örnek 2 belirli bir anahtarın IotHub ConnectionString Ifadesini alma</span><span class="sxs-lookup"><span data-stu-id="4c4b7-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="4c4b7-112">"Myiothub" adlı iothub "myKey" adlı anahtarın ConnectionString öğesini alır</span><span class="sxs-lookup"><span data-stu-id="4c4b7-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="4c4b7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c4b7-113">PARAMETERS</span></span>

### <span data-ttu-id="4c4b7-114">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="4c4b7-114">-KeyName</span></span>
<span data-ttu-id="4c4b7-115">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="4c4b7-115">Name of the Key</span></span>

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

### <span data-ttu-id="4c4b7-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c4b7-116">-Name</span></span>
<span data-ttu-id="4c4b7-117">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="4c4b7-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="4c4b7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c4b7-118">-ResourceGroupName</span></span>
<span data-ttu-id="4c4b7-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4c4b7-119">Resource Group Name</span></span>

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

### <span data-ttu-id="4c4b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c4b7-120">-DefaultProfile</span></span>
<span data-ttu-id="4c4b7-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c4b7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c4b7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c4b7-122">CommonParameters</span></span>
<span data-ttu-id="4c4b7-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c4b7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c4b7-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c4b7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c4b7-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c4b7-125">INPUTS</span></span>

### <span data-ttu-id="4c4b7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4c4b7-126">System.String</span></span>

## <span data-ttu-id="4c4b7-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c4b7-127">OUTPUTS</span></span>

### <span data-ttu-id="4c4b7-128">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="4c4b7-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="4c4b7-129">System. Koleksiyonlar. Generic. LIST \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstif, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="4c4b7-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="4c4b7-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c4b7-130">NOTES</span></span>

## <span data-ttu-id="4c4b7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c4b7-131">RELATED LINKS</span></span>

