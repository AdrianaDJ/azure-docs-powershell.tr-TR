---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106570"
---
# <span data-ttu-id="98dc0-101">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="98dc0-101">Get-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="98dc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="98dc0-103">Azure 'daki Azure RemoteApp sanal ağları hakkında bilgi getirir.</span><span class="sxs-lookup"><span data-stu-id="98dc0-103">Retrieves information about Azure RemoteApp virtual networks in Azure.</span></span>

## <span data-ttu-id="98dc0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98dc0-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="98dc0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98dc0-105">DESCRIPTION</span></span>
<span data-ttu-id="98dc0-106">**Get-AzureRemoteAppVNet** cmdlet 'ı, Microsoft Azure 'Daki Azure RemoteApp sanal ağları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="98dc0-106">The **Get-AzureRemoteAppVNet** cmdlet retrieves information about Azure RemoteApp virtual networks in Microsoft Azure.</span></span>
<span data-ttu-id="98dc0-107">Bu cmdlet, belirtilen sanal ağ hakkında bilgi içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="98dc0-107">This cmdlet returns an object that contains information about a specified virtual network.</span></span>
<span data-ttu-id="98dc0-108">Sanal ağ belirtilmezse, bu cmdlet geçerli abonelikteki tüm sanal ağlarla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="98dc0-108">If no virtual network is specified, this cmdlet returns information about all the virtual networks in the current subscription.</span></span>

## <span data-ttu-id="98dc0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98dc0-109">EXAMPLES</span></span>

### <span data-ttu-id="98dc0-110">Örnek 1: sanal ağ hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="98dc0-110">Example 1: Retrieve information about a virtual network</span></span>
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

<span data-ttu-id="98dc0-111">Bu komut, ContosoVNet adındaki sanal ağ hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="98dc0-111">This command gets information about the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="98dc0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98dc0-112">PARAMETERS</span></span>

### <span data-ttu-id="98dc0-113">-Includesharedkey</span><span class="sxs-lookup"><span data-stu-id="98dc0-113">-IncludeSharedKey</span></span>
<span data-ttu-id="98dc0-114">Bu cmdlet 'in sanal ağ hakkında aldığı bilgilerde paylaşılan anahtar değerini içerdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="98dc0-114">Indicates that this cmdlet includes the shared key value in the information it retrieves about the virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98dc0-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="98dc0-115">-Profile</span></span>
<span data-ttu-id="98dc0-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="98dc0-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98dc0-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="98dc0-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98dc0-118">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="98dc0-118">-VNetName</span></span>
<span data-ttu-id="98dc0-119">Azure RemoteApp sanal ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98dc0-119">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="98dc0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98dc0-120">CommonParameters</span></span>
<span data-ttu-id="98dc0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98dc0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98dc0-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98dc0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98dc0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98dc0-123">INPUTS</span></span>

## <span data-ttu-id="98dc0-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98dc0-124">OUTPUTS</span></span>

## <span data-ttu-id="98dc0-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98dc0-125">NOTES</span></span>

## <span data-ttu-id="98dc0-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98dc0-126">RELATED LINKS</span></span>

[<span data-ttu-id="98dc0-127">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="98dc0-127">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


