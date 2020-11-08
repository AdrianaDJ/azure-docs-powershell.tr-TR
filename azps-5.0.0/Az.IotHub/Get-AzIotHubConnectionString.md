---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277757"
---
# <span data-ttu-id="05c70-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="05c70-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="05c70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05c70-102">SYNOPSIS</span></span>
<span data-ttu-id="05c70-103">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="05c70-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="05c70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05c70-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05c70-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="05c70-105">DESCRIPTION</span></span>
<span data-ttu-id="05c70-106">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="05c70-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="05c70-107">Tüm anahtarlar için ConnectionString veya belirli bir anahtar adına göre filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05c70-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="05c70-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05c70-108">EXAMPLES</span></span>

### <span data-ttu-id="05c70-109">Örnek 1 tüm IotHub ConnectionString Ifadesini al</span><span class="sxs-lookup"><span data-stu-id="05c70-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="05c70-110">"Myiothub" adındaki iothub tüm anahtarlarının ConnectionString 'i alır</span><span class="sxs-lookup"><span data-stu-id="05c70-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="05c70-111">Örnek 2 belirli bir anahtarın IotHub ConnectionString Ifadesini alma</span><span class="sxs-lookup"><span data-stu-id="05c70-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="05c70-112">"Myiothub" adlı iothub "myKey" adlı anahtarın ConnectionString öğesini alır</span><span class="sxs-lookup"><span data-stu-id="05c70-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="05c70-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05c70-113">PARAMETERS</span></span>

### <span data-ttu-id="05c70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c70-114">-DefaultProfile</span></span>
<span data-ttu-id="05c70-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="05c70-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05c70-116">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="05c70-116">-KeyName</span></span>
<span data-ttu-id="05c70-117">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="05c70-117">Name of the Key</span></span>

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

### <span data-ttu-id="05c70-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="05c70-118">-Name</span></span>
<span data-ttu-id="05c70-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="05c70-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="05c70-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c70-120">-ResourceGroupName</span></span>
<span data-ttu-id="05c70-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="05c70-121">Resource Group Name</span></span>

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

### <span data-ttu-id="05c70-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c70-122">CommonParameters</span></span>
<span data-ttu-id="05c70-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05c70-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c70-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05c70-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c70-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05c70-125">INPUTS</span></span>

### <span data-ttu-id="05c70-126">System. String</span><span class="sxs-lookup"><span data-stu-id="05c70-126">System.String</span></span>

## <span data-ttu-id="05c70-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05c70-127">OUTPUTS</span></span>

### <span data-ttu-id="05c70-128">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="05c70-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="05c70-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05c70-129">NOTES</span></span>

## <span data-ttu-id="05c70-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05c70-130">RELATED LINKS</span></span>
