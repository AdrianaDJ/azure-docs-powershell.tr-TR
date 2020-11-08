---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097370"
---
# <span data-ttu-id="efcad-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="efcad-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="efcad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efcad-102">SYNOPSIS</span></span>
<span data-ttu-id="efcad-103">Bir IotHub anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="efcad-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="efcad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efcad-104">SYNTAX</span></span>

### <span data-ttu-id="efcad-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="efcad-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efcad-106">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="efcad-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="efcad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="efcad-107">DESCRIPTION</span></span>
<span data-ttu-id="efcad-108">Bir IotHub anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="efcad-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="efcad-109">Tüm anahtarları listeleyebilir veya listeyi belirli bir anahtar adına göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="efcad-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="efcad-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efcad-110">EXAMPLES</span></span>

### <span data-ttu-id="efcad-111">Örnek 1 tüm tuşları al</span><span class="sxs-lookup"><span data-stu-id="efcad-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="efcad-112">"Myiothub" adındaki IotHub için tüm tuşları alır</span><span class="sxs-lookup"><span data-stu-id="efcad-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="efcad-113">Örnek 2 belirli bir anahtarla ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="efcad-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="efcad-114">"Myiothub" adlı IotHub "ıothubowner" adlı bir anahtarın bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="efcad-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="efcad-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efcad-115">PARAMETERS</span></span>

### <span data-ttu-id="efcad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efcad-116">-DefaultProfile</span></span>
<span data-ttu-id="efcad-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="efcad-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efcad-118">-Hubıd</span><span class="sxs-lookup"><span data-stu-id="efcad-118">-HubId</span></span>
<span data-ttu-id="efcad-119">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="efcad-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="efcad-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="efcad-120">-KeyName</span></span>
<span data-ttu-id="efcad-121">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="efcad-121">Name of the Key</span></span>

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

### <span data-ttu-id="efcad-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="efcad-122">-Name</span></span>
<span data-ttu-id="efcad-123">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="efcad-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="efcad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efcad-124">-ResourceGroupName</span></span>
<span data-ttu-id="efcad-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="efcad-125">Resource Group Name</span></span>

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

### <span data-ttu-id="efcad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efcad-126">CommonParameters</span></span>
<span data-ttu-id="efcad-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="efcad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efcad-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efcad-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efcad-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efcad-129">INPUTS</span></span>

### <span data-ttu-id="efcad-130">System. String</span><span class="sxs-lookup"><span data-stu-id="efcad-130">System.String</span></span>

## <span data-ttu-id="efcad-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efcad-131">OUTPUTS</span></span>

### <span data-ttu-id="efcad-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="efcad-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="efcad-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efcad-133">NOTES</span></span>

## <span data-ttu-id="efcad-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efcad-134">RELATED LINKS</span></span>