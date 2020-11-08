---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D50984B7-FD97-4713-8E56-1C06D2B008E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: a01d59d6a0755b3763eaef9b7532326ca0ffd402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105779"
---
# <span data-ttu-id="2a06a-101">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a06a-101">Start-AzureApplicationGateway</span></span>

## <span data-ttu-id="2a06a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a06a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a06a-103">Uygulama ağ geçidi başlatır.</span><span class="sxs-lookup"><span data-stu-id="2a06a-103">Starts an application gateway.</span></span>

## <span data-ttu-id="2a06a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a06a-104">SYNTAX</span></span>

```
Start-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2a06a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a06a-105">DESCRIPTION</span></span>
<span data-ttu-id="2a06a-106">**Start-AzureApplicationGateway** cmdlet 'i bir uygulama ağ geçidi başlatır.</span><span class="sxs-lookup"><span data-stu-id="2a06a-106">The **Start-AzureApplicationGateway** cmdlet starts an application gateway.</span></span>

## <span data-ttu-id="2a06a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a06a-107">EXAMPLES</span></span>

### <span data-ttu-id="2a06a-108">Örnek 1: uygulama ağ geçidi başlatma</span><span class="sxs-lookup"><span data-stu-id="2a06a-108">Example 1: Start an application gateway</span></span>
```
PS C:\> Start-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="2a06a-109">Bu komut ApplicationGateway06 adlı uygulama ağ geçidini başlatır.</span><span class="sxs-lookup"><span data-stu-id="2a06a-109">This command starts the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="2a06a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a06a-110">PARAMETERS</span></span>

### <span data-ttu-id="2a06a-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a06a-111">-Name</span></span>
<span data-ttu-id="2a06a-112">Bu cmdlet 'in başladığı uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a06a-112">Specifies the name of the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="2a06a-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="2a06a-113">-Profile</span></span>
<span data-ttu-id="2a06a-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a06a-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2a06a-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2a06a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2a06a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a06a-116">CommonParameters</span></span>
<span data-ttu-id="2a06a-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a06a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a06a-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a06a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a06a-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a06a-119">INPUTS</span></span>

### <span data-ttu-id="2a06a-120">System. String</span><span class="sxs-lookup"><span data-stu-id="2a06a-120">System.String</span></span>

## <span data-ttu-id="2a06a-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a06a-121">OUTPUTS</span></span>

### <span data-ttu-id="2a06a-122">Microsoft. Windowsazme. Management. ApplicationGateway. model. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2a06a-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="2a06a-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a06a-123">NOTES</span></span>

## <span data-ttu-id="2a06a-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a06a-124">RELATED LINKS</span></span>

[<span data-ttu-id="2a06a-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a06a-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="2a06a-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a06a-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="2a06a-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a06a-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="2a06a-128">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a06a-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="2a06a-129">Güncelleştirme-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a06a-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


