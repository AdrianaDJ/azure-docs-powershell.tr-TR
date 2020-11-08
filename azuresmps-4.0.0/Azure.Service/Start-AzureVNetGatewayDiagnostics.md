---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106026"
---
# <span data-ttu-id="bb09f-101">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bb09f-101">Start-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="bb09f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb09f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb09f-103">VPN ağ geçidi için ağ geçidi tanılaması başlatır.</span><span class="sxs-lookup"><span data-stu-id="bb09f-103">Starts gateway diagnostics for a VPN gateway.</span></span>

## <span data-ttu-id="bb09f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb09f-104">SYNTAX</span></span>

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb09f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb09f-105">DESCRIPTION</span></span>
<span data-ttu-id="bb09f-106">**Start-AzureVNetGatewayDiagnostics** cmdlet 'i sanal özel ağ (VPN) ağ geçidi için yeni bir ağ geçidi tanılama oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="bb09f-106">The **Start-AzureVNetGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual private network (VPN) gateway.</span></span>
<span data-ttu-id="bb09f-107">Aynı anda yalnızca bir ağ geçidi tanılama oturumu çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="bb09f-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="bb09f-108">Ağ geçidi tanılama oturumu çalışırken bu cmdlet 'i çalıştırırsanız, bu cmdlet bir hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb09f-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="bb09f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb09f-109">EXAMPLES</span></span>

## <span data-ttu-id="bb09f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb09f-110">PARAMETERS</span></span>

### <span data-ttu-id="bb09f-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="bb09f-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="bb09f-112">Yakalama süresini saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb09f-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb09f-113">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="bb09f-113">-ContainerName</span></span>
<span data-ttu-id="bb09f-114">Bir Azure kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb09f-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="bb09f-115">Bu cmdlet sonuçları bu parametrenin belirttiği kapsayıcıda depolar.</span><span class="sxs-lookup"><span data-stu-id="bb09f-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb09f-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="bb09f-116">-Profile</span></span>
<span data-ttu-id="bb09f-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb09f-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bb09f-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="bb09f-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bb09f-119">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="bb09f-119">-StorageContext</span></span>
<span data-ttu-id="bb09f-120">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb09f-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bb09f-121">Bu cmdlet, bu parametrenin belirttiği depolama bağlamını kullanarak sonuçları depolar.</span><span class="sxs-lookup"><span data-stu-id="bb09f-121">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb09f-122">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="bb09f-122">-VNetName</span></span>
<span data-ttu-id="bb09f-123">Bu cmdlet 'in tanılama çalıştırdığı sanal ağ geçidi içeren sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb09f-123">Specifies the virtual network that contains a virtual network gateway for which this cmdlet runs diagnostics.</span></span>

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

### <span data-ttu-id="bb09f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb09f-124">CommonParameters</span></span>
<span data-ttu-id="bb09f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb09f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb09f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb09f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb09f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb09f-127">INPUTS</span></span>

## <span data-ttu-id="bb09f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb09f-128">OUTPUTS</span></span>

## <span data-ttu-id="bb09f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb09f-129">NOTES</span></span>

## <span data-ttu-id="bb09f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb09f-130">RELATED LINKS</span></span>

[<span data-ttu-id="bb09f-131">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bb09f-131">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="bb09f-132">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bb09f-132">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


