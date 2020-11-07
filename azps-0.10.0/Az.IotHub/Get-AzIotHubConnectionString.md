---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: 92d1e3f2ef1ba87a5e9683f7ac6617e31bb8a055
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935844"
---
# <span data-ttu-id="88cee-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="88cee-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="88cee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88cee-102">SYNOPSIS</span></span>
<span data-ttu-id="88cee-103">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="88cee-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="88cee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88cee-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88cee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88cee-105">DESCRIPTION</span></span>
<span data-ttu-id="88cee-106">IotHub ConnectionString 'i alır.</span><span class="sxs-lookup"><span data-stu-id="88cee-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="88cee-107">Tüm anahtarlar için ConnectionString veya belirli bir anahtar adına göre filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="88cee-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="88cee-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88cee-108">EXAMPLES</span></span>

### <span data-ttu-id="88cee-109">Örnek 1 tüm IotHub ConnectionString Ifadesini al</span><span class="sxs-lookup"><span data-stu-id="88cee-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="88cee-110">"Myiothub" adındaki iothub tüm anahtarlarının ConnectionString 'i alır</span><span class="sxs-lookup"><span data-stu-id="88cee-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="88cee-111">Örnek 2 belirli bir anahtarın IotHub ConnectionString Ifadesini alma</span><span class="sxs-lookup"><span data-stu-id="88cee-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="88cee-112">"Myiothub" adlı iothub "myKey" adlı anahtarın ConnectionString öğesini alır</span><span class="sxs-lookup"><span data-stu-id="88cee-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="88cee-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88cee-113">PARAMETERS</span></span>

### <span data-ttu-id="88cee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88cee-114">-DefaultProfile</span></span>
<span data-ttu-id="88cee-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="88cee-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88cee-116">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="88cee-116">-KeyName</span></span>
<span data-ttu-id="88cee-117">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="88cee-117">Name of the Key</span></span>

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

### <span data-ttu-id="88cee-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="88cee-118">-Name</span></span>
<span data-ttu-id="88cee-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="88cee-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="88cee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88cee-120">-ResourceGroupName</span></span>
<span data-ttu-id="88cee-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="88cee-121">Resource Group Name</span></span>

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

### <span data-ttu-id="88cee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88cee-122">CommonParameters</span></span>
<span data-ttu-id="88cee-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88cee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88cee-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88cee-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88cee-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88cee-125">INPUTS</span></span>

### <span data-ttu-id="88cee-126">System. String</span><span class="sxs-lookup"><span data-stu-id="88cee-126">System.String</span></span>

## <span data-ttu-id="88cee-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88cee-127">OUTPUTS</span></span>

### <span data-ttu-id="88cee-128">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="88cee-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="88cee-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88cee-129">NOTES</span></span>

## <span data-ttu-id="88cee-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88cee-130">RELATED LINKS</span></span>
