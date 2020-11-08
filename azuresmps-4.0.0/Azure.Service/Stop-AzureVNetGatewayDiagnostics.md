---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106019"
---
# <span data-ttu-id="a35d9-101">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a35d9-101">Stop-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="a35d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a35d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a35d9-103">Çalışan bir VPN ağ geçidi tanılama oturumunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="a35d9-103">Stops a running VPN gateway diagnostics session.</span></span>

## <span data-ttu-id="a35d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a35d9-104">SYNTAX</span></span>

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a35d9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a35d9-105">DESCRIPTION</span></span>
<span data-ttu-id="a35d9-106">**Stop-AzureVNetGatewayDiagnostics** cmdlet 'i, çalışan bir sanal özel ağ (VPN) ağ geçidi tanılama oturumunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="a35d9-106">The **Stop-AzureVNetGatewayDiagnostics** cmdlet stops a running virtual private network (VPN) gateway diagnostics session.</span></span>
<span data-ttu-id="a35d9-107">Bu komut tanılama oturumunun sonuçlarını **Start-AzureVNetGatewayDiagnostics** cmdlet 'inin belirttiği depolama hesabına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="a35d9-107">This command saves the results of the diagnostics session to the storage account that the **Start-AzureVNetGatewayDiagnostics** cmdlet specifies.</span></span>

## <span data-ttu-id="a35d9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a35d9-108">EXAMPLES</span></span>

## <span data-ttu-id="a35d9-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a35d9-109">PARAMETERS</span></span>

### <span data-ttu-id="a35d9-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="a35d9-110">-Profile</span></span>
<span data-ttu-id="a35d9-111">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a35d9-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a35d9-112">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a35d9-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a35d9-113">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="a35d9-113">-VNetName</span></span>
<span data-ttu-id="a35d9-114">Bu cmdlet 'in tanılama işlemini durdurduğu sanal ağ geçidi içeren sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a35d9-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet stops diagnostics.</span></span>

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

### <span data-ttu-id="a35d9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35d9-115">CommonParameters</span></span>
<span data-ttu-id="a35d9-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a35d9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35d9-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a35d9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35d9-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a35d9-118">INPUTS</span></span>

## <span data-ttu-id="a35d9-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a35d9-119">OUTPUTS</span></span>

## <span data-ttu-id="a35d9-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a35d9-120">NOTES</span></span>

## <span data-ttu-id="a35d9-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a35d9-121">RELATED LINKS</span></span>

[<span data-ttu-id="a35d9-122">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a35d9-122">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="a35d9-123">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a35d9-123">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)


