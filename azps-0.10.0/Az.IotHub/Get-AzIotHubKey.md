---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 29f9fc8847e4b8bf3ab348fcad8f312dab71fd0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935839"
---
# <span data-ttu-id="ce0dc-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="ce0dc-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="ce0dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce0dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0dc-103">Bir IotHub anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="ce0dc-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="ce0dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce0dc-104">SYNTAX</span></span>

### <span data-ttu-id="ce0dc-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ce0dc-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce0dc-106">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="ce0dc-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce0dc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce0dc-107">DESCRIPTION</span></span>
<span data-ttu-id="ce0dc-108">Bir IotHub anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="ce0dc-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="ce0dc-109">Tüm anahtarları listeleyebilir veya listeyi belirli bir anahtar adına göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce0dc-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="ce0dc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce0dc-110">EXAMPLES</span></span>

### <span data-ttu-id="ce0dc-111">Örnek 1 tüm tuşları al</span><span class="sxs-lookup"><span data-stu-id="ce0dc-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ce0dc-112">"Myiothub" adındaki IotHub için tüm tuşları alır</span><span class="sxs-lookup"><span data-stu-id="ce0dc-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="ce0dc-113">Örnek 2 belirli bir anahtarla ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="ce0dc-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="ce0dc-114">"Myiothub" adlı IotHub "ıothubowner" adlı bir anahtarın bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="ce0dc-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ce0dc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce0dc-115">PARAMETERS</span></span>

### <span data-ttu-id="ce0dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0dc-116">-DefaultProfile</span></span>
<span data-ttu-id="ce0dc-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ce0dc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce0dc-118">-Hubıd</span><span class="sxs-lookup"><span data-stu-id="ce0dc-118">-HubId</span></span>
<span data-ttu-id="ce0dc-119">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ce0dc-119">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce0dc-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="ce0dc-120">-KeyName</span></span>
<span data-ttu-id="ce0dc-121">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="ce0dc-121">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0dc-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce0dc-122">-Name</span></span>
<span data-ttu-id="ce0dc-123">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="ce0dc-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce0dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce0dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce0dc-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ce0dc-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce0dc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0dc-126">CommonParameters</span></span>
<span data-ttu-id="ce0dc-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce0dc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0dc-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce0dc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0dc-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce0dc-129">INPUTS</span></span>

### <span data-ttu-id="ce0dc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ce0dc-130">System.String</span></span>

## <span data-ttu-id="ce0dc-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce0dc-131">OUTPUTS</span></span>

### <span data-ttu-id="ce0dc-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="ce0dc-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="ce0dc-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce0dc-133">NOTES</span></span>

## <span data-ttu-id="ce0dc-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce0dc-134">RELATED LINKS</span></span>
