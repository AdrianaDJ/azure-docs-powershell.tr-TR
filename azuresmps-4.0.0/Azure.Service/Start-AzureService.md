---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 821CB3E4-102E-440A-8C92-D1890899A6EE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 64924d579eebb826bc9c36468da1617370f48cf7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106030"
---
# <span data-ttu-id="bbb9a-101">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="bbb9a-101">Start-AzureService</span></span>

## <span data-ttu-id="bbb9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbb9a-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb9a-103">Windows Azure 'da belirtilen barındırılan hizmeti başlatır.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-103">Starts the specified hosted service in Windows Azure.</span></span>

## <span data-ttu-id="bbb9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbb9a-104">SYNTAX</span></span>

```
Start-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbb9a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbb9a-105">DESCRIPTION</span></span>
<span data-ttu-id="bbb9a-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bbb9a-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bbb9a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bbb9a-108">Hizmet durdurulmuş durumdaysa, **Start-AzureService** cmdlet 'ı Windows Azure 'da belirtilen barındırılan hizmeti başlatır.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-108">The **Start-AzureService** cmdlet starts the specified hosted service in Windows Azure, if the service is in the stopped state.</span></span>
<span data-ttu-id="bbb9a-109">**Publish-AzureServiceProject** cmdlet 'inin hizmeti otomatik olarak başlatmaya çalıştığı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-109">Note that the **Publish-AzureServiceProject** cmdlet automatically attempts to start the service.</span></span>

## <span data-ttu-id="bbb9a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbb9a-110">EXAMPLES</span></span>

## <span data-ttu-id="bbb9a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbb9a-111">PARAMETERS</span></span>

### <span data-ttu-id="bbb9a-112">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bbb9a-112">-PassThru</span></span>
<span data-ttu-id="bbb9a-113">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bbb9a-114">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bbb9a-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="bbb9a-115">-Profile</span></span>
<span data-ttu-id="bbb9a-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bbb9a-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bbb9a-118">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="bbb9a-118">-ServiceName</span></span>
<span data-ttu-id="bbb9a-119">Başlayacak barındırılan hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-119">Specifies the name of the hosted service to start.</span></span>
<span data-ttu-id="bbb9a-120">Ad belirtilmezse cmdlet, geçerli barındırılan hizmeti başlatır.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-120">If no name is specified, the cmdlet starts the current hosted service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb9a-121">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="bbb9a-121">-Slot</span></span>
<span data-ttu-id="bbb9a-122">Servisi başlatmak istediğiniz dağıtım yuvasını, basamaklandırma veya üretim olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-122">Specifies the deployment slot in which to start the service, either Staging or Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb9a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb9a-123">CommonParameters</span></span>
<span data-ttu-id="bbb9a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbb9a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb9a-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbb9a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb9a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbb9a-126">INPUTS</span></span>

## <span data-ttu-id="bbb9a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbb9a-127">OUTPUTS</span></span>

## <span data-ttu-id="bbb9a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbb9a-128">NOTES</span></span>

## <span data-ttu-id="bbb9a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbb9a-129">RELATED LINKS</span></span>

[<span data-ttu-id="bbb9a-130">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="bbb9a-130">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="bbb9a-131">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="bbb9a-131">Start-AzureService</span></span>](./Start-AzureService.md)

[<span data-ttu-id="bbb9a-132">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="bbb9a-132">Stop-AzureService</span></span>](./Stop-AzureService.md)


