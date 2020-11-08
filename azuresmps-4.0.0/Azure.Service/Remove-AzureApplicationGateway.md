---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106497"
---
# <span data-ttu-id="0bd5b-101">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0bd5b-101">Remove-AzureApplicationGateway</span></span>

## <span data-ttu-id="0bd5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd5b-103">Uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0bd5b-103">Removes an application gateway.</span></span>

## <span data-ttu-id="0bd5b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0bd5b-104">SYNTAX</span></span>

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0bd5b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0bd5b-105">DESCRIPTION</span></span>
<span data-ttu-id="0bd5b-106">**Remove-AzureApplicationGateway** cmdlet 'i uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0bd5b-106">The **Remove-AzureApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="0bd5b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0bd5b-107">EXAMPLES</span></span>

### <span data-ttu-id="0bd5b-108">Örnek 1: uygulama ağ geçidini kaldırma</span><span class="sxs-lookup"><span data-stu-id="0bd5b-108">Example 1: Remove an application gateway</span></span>
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="0bd5b-109">Bu komut, ApplicationGateway06 adlı uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0bd5b-109">This command removes the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="0bd5b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0bd5b-110">PARAMETERS</span></span>

### <span data-ttu-id="0bd5b-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="0bd5b-111">-Name</span></span>
<span data-ttu-id="0bd5b-112">Bu cmdlet 'in kaldırdığı uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bd5b-112">Specifies the name of the application gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0bd5b-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="0bd5b-113">-Profile</span></span>
<span data-ttu-id="0bd5b-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bd5b-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0bd5b-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0bd5b-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0bd5b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd5b-116">CommonParameters</span></span>
<span data-ttu-id="0bd5b-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0bd5b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd5b-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bd5b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd5b-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0bd5b-119">INPUTS</span></span>

### <span data-ttu-id="0bd5b-120">System. String</span><span class="sxs-lookup"><span data-stu-id="0bd5b-120">System.String</span></span>

## <span data-ttu-id="0bd5b-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0bd5b-121">OUTPUTS</span></span>

### <span data-ttu-id="0bd5b-122">Microsoft. Windowsazme. Management. ApplicationGateway. model. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0bd5b-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="0bd5b-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0bd5b-123">NOTES</span></span>

## <span data-ttu-id="0bd5b-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0bd5b-124">RELATED LINKS</span></span>

[<span data-ttu-id="0bd5b-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0bd5b-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="0bd5b-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0bd5b-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="0bd5b-127">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0bd5b-127">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="0bd5b-128">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0bd5b-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="0bd5b-129">Güncelleştirme-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0bd5b-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


