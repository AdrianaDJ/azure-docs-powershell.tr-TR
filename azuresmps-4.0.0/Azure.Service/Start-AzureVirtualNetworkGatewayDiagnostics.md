---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105772"
---
# <span data-ttu-id="aded8-101">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="aded8-101">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="aded8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aded8-102">SYNOPSIS</span></span>
<span data-ttu-id="aded8-103">Sanal ağ geçidi tanılaması başlatır.</span><span class="sxs-lookup"><span data-stu-id="aded8-103">Starts diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="aded8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aded8-104">SYNTAX</span></span>

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="aded8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aded8-105">DESCRIPTION</span></span>
<span data-ttu-id="aded8-106">**Start-AzureVirtualNetworkGatewayDiagnostics** cmdlet 'i sanal ağ geçidi için yeni bir ağ geçidi tanılama oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="aded8-106">The **Start-AzureVirtualNetworkGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual network gateway.</span></span>
<span data-ttu-id="aded8-107">Aynı anda yalnızca bir ağ geçidi tanılama oturumu çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="aded8-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="aded8-108">Ağ geçidi tanılama oturumu çalışırken bu cmdlet 'i çalıştırırsanız, bu cmdlet bir hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="aded8-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="aded8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aded8-109">EXAMPLES</span></span>

## <span data-ttu-id="aded8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aded8-110">PARAMETERS</span></span>

### <span data-ttu-id="aded8-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="aded8-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="aded8-112">Yakalama süresini saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="aded8-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aded8-113">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="aded8-113">-ContainerName</span></span>
<span data-ttu-id="aded8-114">Bir Azure kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aded8-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="aded8-115">Bu cmdlet sonuçları bu parametrenin belirttiği kapsayıcıda depolar.</span><span class="sxs-lookup"><span data-stu-id="aded8-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aded8-116">-Gatewayıd</span><span class="sxs-lookup"><span data-stu-id="aded8-116">-GatewayId</span></span>
<span data-ttu-id="aded8-117">Ağ geçidinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="aded8-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="aded8-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="aded8-118">-Profile</span></span>
<span data-ttu-id="aded8-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aded8-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="aded8-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="aded8-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aded8-121">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="aded8-121">-StorageContext</span></span>
<span data-ttu-id="aded8-122">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aded8-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="aded8-123">Bu cmdlet, bu parametrenin belirttiği depolama bağlamını kullanarak sonuçları depolar.</span><span class="sxs-lookup"><span data-stu-id="aded8-123">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aded8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aded8-124">CommonParameters</span></span>
<span data-ttu-id="aded8-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aded8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aded8-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aded8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aded8-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aded8-127">INPUTS</span></span>

## <span data-ttu-id="aded8-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aded8-128">OUTPUTS</span></span>

## <span data-ttu-id="aded8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aded8-129">NOTES</span></span>

## <span data-ttu-id="aded8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aded8-130">RELATED LINKS</span></span>

[<span data-ttu-id="aded8-131">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="aded8-131">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="aded8-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="aded8-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


