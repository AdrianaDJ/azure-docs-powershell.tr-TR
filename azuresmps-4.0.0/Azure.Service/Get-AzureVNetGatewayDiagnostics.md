---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106277"
---
# <span data-ttu-id="b06ee-101">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b06ee-101">Get-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="b06ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b06ee-102">SYNOPSIS</span></span>
<span data-ttu-id="b06ee-103">Sanal ağ geçidi tanılaması 'nın geçerli durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="b06ee-103">Gets the current state of diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="b06ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b06ee-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b06ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b06ee-105">DESCRIPTION</span></span>
<span data-ttu-id="b06ee-106">**Get-AzureVNetGatewayDiagnostics** cmdlet 'i sanal ağ geçidi için tanılamaların geçerli durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="b06ee-106">The **Get-AzureVNetGatewayDiagnostics** cmdlet gets the current state of diagnostics for a virtual network gateway.</span></span>
<span data-ttu-id="b06ee-107">**Start-AzureVNetGatewayDiagnostics** ' ı bir önceki tanılama oturumunu kaydettiği bir ikili büyük nesne (blob) varsa, bu cmdlet bu cmdlet 'in Bu tanılama oturumunu KAYDETTIĞI blob URL 'sini de döndürür.</span><span class="sxs-lookup"><span data-stu-id="b06ee-107">If a binary large object (blob) exists where the **Start-AzureVNetGatewayDiagnostics** saved a previous diagnostics session, this cmdlet also returns the URL of the blob where that cmdlet saved that diagnostics session.</span></span>

## <span data-ttu-id="b06ee-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b06ee-108">EXAMPLES</span></span>

## <span data-ttu-id="b06ee-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b06ee-109">PARAMETERS</span></span>

### <span data-ttu-id="b06ee-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="b06ee-110">-Profile</span></span>
<span data-ttu-id="b06ee-111">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b06ee-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b06ee-112">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b06ee-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b06ee-113">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="b06ee-113">-VNetName</span></span>
<span data-ttu-id="b06ee-114">Bu cmdlet 'in tanılama aldığı sanal ağ geçidi içeren sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b06ee-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet gets diagnostics.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06ee-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06ee-115">CommonParameters</span></span>
<span data-ttu-id="b06ee-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b06ee-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06ee-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b06ee-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06ee-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b06ee-118">INPUTS</span></span>

## <span data-ttu-id="b06ee-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b06ee-119">OUTPUTS</span></span>

## <span data-ttu-id="b06ee-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b06ee-120">NOTES</span></span>

## <span data-ttu-id="b06ee-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b06ee-121">RELATED LINKS</span></span>

[<span data-ttu-id="b06ee-122">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b06ee-122">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="b06ee-123">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b06ee-123">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


