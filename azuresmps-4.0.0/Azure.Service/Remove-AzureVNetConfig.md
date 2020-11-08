---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D903741F-1D22-48FC-BFA5-6876E557EFE5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4284d34ef5151dbcd16d9ed882dcf112abbb8ea5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105492"
---
# <span data-ttu-id="2f002-101">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="2f002-101">Remove-AzureVNetConfig</span></span>

## <span data-ttu-id="2f002-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f002-102">SYNOPSIS</span></span>
<span data-ttu-id="2f002-103">Geçerli Azure aboneliğinden ağ yapılandırmasını siler.</span><span class="sxs-lookup"><span data-stu-id="2f002-103">Deletes the network configuration from the current Azure subscription.</span></span>

## <span data-ttu-id="2f002-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f002-104">SYNTAX</span></span>

```
Remove-AzureVNetConfig [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2f002-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f002-105">DESCRIPTION</span></span>
<span data-ttu-id="2f002-106">**Remove-AzureVNetConfig** cmdlet 'ı geçerli Azure aboneliğindeki tüm sanal ağ ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2f002-106">The **Remove-AzureVNetConfig** cmdlet removes all virtual network settings from the current Azure subscription.</span></span>

## <span data-ttu-id="2f002-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f002-107">EXAMPLES</span></span>

### <span data-ttu-id="2f002-108">Örnek 1: geçerli abonelikten sanal ağ yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="2f002-108">Example 1: Remove a virtual network configuration from the current subscription</span></span>
```
PS C:\> Remove-AzureVNetConfig
```

<span data-ttu-id="2f002-109">Bu komut, geçerli abonelikteki sanal ağ yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2f002-109">This command removes the virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="2f002-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f002-110">PARAMETERS</span></span>

### <span data-ttu-id="2f002-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="2f002-111">-InformationAction</span></span>
<span data-ttu-id="2f002-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f002-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2f002-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2f002-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f002-114">'A</span><span class="sxs-lookup"><span data-stu-id="2f002-114">Continue</span></span>
- <span data-ttu-id="2f002-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="2f002-115">Ignore</span></span>
- <span data-ttu-id="2f002-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="2f002-116">Inquire</span></span>
- <span data-ttu-id="2f002-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="2f002-117">SilentlyContinue</span></span>
- <span data-ttu-id="2f002-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="2f002-118">Stop</span></span>
- <span data-ttu-id="2f002-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="2f002-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f002-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="2f002-120">-InformationVariable</span></span>
<span data-ttu-id="2f002-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f002-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f002-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="2f002-122">-Profile</span></span>
<span data-ttu-id="2f002-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f002-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f002-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2f002-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2f002-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f002-125">CommonParameters</span></span>
<span data-ttu-id="2f002-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f002-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f002-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f002-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f002-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f002-128">INPUTS</span></span>

## <span data-ttu-id="2f002-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f002-129">OUTPUTS</span></span>

## <span data-ttu-id="2f002-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f002-130">NOTES</span></span>

## <span data-ttu-id="2f002-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f002-131">RELATED LINKS</span></span>

[<span data-ttu-id="2f002-132">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="2f002-132">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="2f002-133">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="2f002-133">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="2f002-134">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="2f002-134">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


