---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f89d47dac0b48ca82b2478743d2993f94fb792d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916479"
---
# <span data-ttu-id="bfdda-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="bfdda-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="bfdda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfdda-102">SYNOPSIS</span></span>
<span data-ttu-id="bfdda-103">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="bfdda-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="bfdda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfdda-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfdda-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfdda-105">DESCRIPTION</span></span>
<span data-ttu-id="bfdda-106">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="bfdda-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="bfdda-107">Tüm anahtarlar için ConnectionString veya belirli bir anahtar adına göre filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bfdda-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="bfdda-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfdda-108">EXAMPLES</span></span>

### <span data-ttu-id="bfdda-109">Örnek 1 tüm IotHub ConnectionString Ifadesini al</span><span class="sxs-lookup"><span data-stu-id="bfdda-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="bfdda-110">"Myiothub" adındaki iothub tüm anahtarlarının ConnectionString 'i alır</span><span class="sxs-lookup"><span data-stu-id="bfdda-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="bfdda-111">Örnek 2 belirli bir anahtarın IotHub ConnectionString Ifadesini alma</span><span class="sxs-lookup"><span data-stu-id="bfdda-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="bfdda-112">"Myiothub" adlı iothub "myKey" adlı anahtarın ConnectionString öğesini alır</span><span class="sxs-lookup"><span data-stu-id="bfdda-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="bfdda-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfdda-113">PARAMETERS</span></span>

### <span data-ttu-id="bfdda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfdda-114">-DefaultProfile</span></span>
<span data-ttu-id="bfdda-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bfdda-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfdda-116">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="bfdda-116">-KeyName</span></span>
<span data-ttu-id="bfdda-117">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="bfdda-117">Name of the Key</span></span>

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

### <span data-ttu-id="bfdda-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="bfdda-118">-Name</span></span>
<span data-ttu-id="bfdda-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="bfdda-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="bfdda-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfdda-120">-ResourceGroupName</span></span>
<span data-ttu-id="bfdda-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bfdda-121">Resource Group Name</span></span>

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

### <span data-ttu-id="bfdda-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfdda-122">CommonParameters</span></span>
<span data-ttu-id="bfdda-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfdda-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfdda-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfdda-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfdda-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfdda-125">INPUTS</span></span>

### <span data-ttu-id="bfdda-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bfdda-126">System.String</span></span>

## <span data-ttu-id="bfdda-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfdda-127">OUTPUTS</span></span>

### <span data-ttu-id="bfdda-128">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="bfdda-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="bfdda-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfdda-129">NOTES</span></span>

## <span data-ttu-id="bfdda-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfdda-130">RELATED LINKS</span></span>
