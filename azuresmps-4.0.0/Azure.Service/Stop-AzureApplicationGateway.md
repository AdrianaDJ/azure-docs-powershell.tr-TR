---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 17BA2ED5-E347-45C0-AF20-CDD288469514
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07afcadb2207f2e4377601abfa6094bc3293328
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106408"
---
# <span data-ttu-id="8db20-101">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8db20-101">Stop-AzureApplicationGateway</span></span>

## <span data-ttu-id="8db20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8db20-102">SYNOPSIS</span></span>
<span data-ttu-id="8db20-103">Uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="8db20-103">Stops an application gateway.</span></span>

## <span data-ttu-id="8db20-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8db20-104">SYNTAX</span></span>

```
Stop-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8db20-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8db20-105">DESCRIPTION</span></span>
<span data-ttu-id="8db20-106">**Stop-AzureApplicationGateway** cmdlet 'i bir uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="8db20-106">The **Stop-AzureApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="8db20-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8db20-107">EXAMPLES</span></span>

### <span data-ttu-id="8db20-108">Örnek 1: uygulama ağ geçidini durdurma</span><span class="sxs-lookup"><span data-stu-id="8db20-108">Example 1: Stop an application gateway</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="8db20-109">Bu komut, ApplicationGateway06 adlı uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="8db20-109">This command stops the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="8db20-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8db20-110">PARAMETERS</span></span>

### <span data-ttu-id="8db20-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="8db20-111">-Name</span></span>
<span data-ttu-id="8db20-112">Bu cmdlet 'in durdurduğu uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8db20-112">Specifies the name of the application gateway that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db20-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="8db20-113">-Profile</span></span>
<span data-ttu-id="8db20-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8db20-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8db20-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8db20-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8db20-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db20-116">CommonParameters</span></span>
<span data-ttu-id="8db20-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8db20-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db20-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8db20-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db20-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8db20-119">INPUTS</span></span>

### <span data-ttu-id="8db20-120">System. String</span><span class="sxs-lookup"><span data-stu-id="8db20-120">System.String</span></span>

## <span data-ttu-id="8db20-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8db20-121">OUTPUTS</span></span>

### <span data-ttu-id="8db20-122">Microsoft. Windowsazme. Management. ApplicationGateway. model. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8db20-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="8db20-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8db20-123">NOTES</span></span>

## <span data-ttu-id="8db20-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8db20-124">RELATED LINKS</span></span>

[<span data-ttu-id="8db20-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8db20-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="8db20-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8db20-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="8db20-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8db20-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="8db20-128">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8db20-128">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="8db20-129">Güncelleştirme-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8db20-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
