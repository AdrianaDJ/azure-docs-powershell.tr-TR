---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B107D789-8F66-4D7D-B126-08ACB0364826
online version: ''
schema: 2.0.0
ms.openlocfilehash: e59df078539e9ea94073defd4c8ea13a69cc2e5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105487"
---
# <span data-ttu-id="f2dad-101">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="f2dad-101">Remove-AzureVirtualIP</span></span>

## <span data-ttu-id="f2dad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2dad-102">SYNOPSIS</span></span>
<span data-ttu-id="f2dad-103">Bulut hizmetinizden sanal IP adresini siler.</span><span class="sxs-lookup"><span data-stu-id="f2dad-103">Deletes a virtual IP address from your Cloud Service.</span></span>

## <span data-ttu-id="f2dad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2dad-104">SYNTAX</span></span>

```
Remove-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f2dad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2dad-105">DESCRIPTION</span></span>
<span data-ttu-id="f2dad-106">**Remove-AzureVirtualIP** cmdlet 'ı bir Azure HIZMETINDEN sanal IP 'YI (VIP) siler.</span><span class="sxs-lookup"><span data-stu-id="f2dad-106">The **Remove-AzureVirtualIP** cmdlet deletes a virtual IP (VIP) from an Azure service.</span></span>
<span data-ttu-id="f2dad-107">İşlem yalnızca sanal IP ile ilişkili uç nokta yoksa başarılı olur.</span><span class="sxs-lookup"><span data-stu-id="f2dad-107">The operation succeeds only if the virtual IP has no endpoints associated with it.</span></span>

## <span data-ttu-id="f2dad-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2dad-108">EXAMPLES</span></span>

### <span data-ttu-id="f2dad-109">Örnek 1: hizmetten sanal IP adresini kaldırma</span><span class="sxs-lookup"><span data-stu-id="f2dad-109">Example 1: Remove a virtual IP address from a service</span></span>
```
PS C:\> Remove-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
```

<span data-ttu-id="f2dad-110">Bu komut, bir hizmetten sanal IP adresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f2dad-110">This command removes a virtual IP address from a service.</span></span>

## <span data-ttu-id="f2dad-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2dad-111">PARAMETERS</span></span>

### <span data-ttu-id="f2dad-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f2dad-112">-Force</span></span>
<span data-ttu-id="f2dad-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f2dad-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2dad-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f2dad-114">-InformationAction</span></span>
<span data-ttu-id="f2dad-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2dad-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f2dad-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f2dad-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2dad-117">'A</span><span class="sxs-lookup"><span data-stu-id="f2dad-117">Continue</span></span>
- <span data-ttu-id="f2dad-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="f2dad-118">Ignore</span></span>
- <span data-ttu-id="f2dad-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f2dad-119">Inquire</span></span>
- <span data-ttu-id="f2dad-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f2dad-120">SilentlyContinue</span></span>
- <span data-ttu-id="f2dad-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f2dad-121">Stop</span></span>
- <span data-ttu-id="f2dad-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f2dad-122">Suspend</span></span>

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

### <span data-ttu-id="f2dad-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f2dad-123">-InformationVariable</span></span>
<span data-ttu-id="f2dad-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2dad-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f2dad-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="f2dad-125">-Profile</span></span>
<span data-ttu-id="f2dad-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2dad-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2dad-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f2dad-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2dad-128">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="f2dad-128">-ServiceName</span></span>
<span data-ttu-id="f2dad-129">Sanal IP adresinin kaldırılacağı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2dad-129">Specifies the name of the service from which to remove a virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2dad-130">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="f2dad-130">-VirtualIPName</span></span>
<span data-ttu-id="f2dad-131">Kaldırılacak sanal IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2dad-131">Specifies the name of the virtual IP address to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2dad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2dad-132">CommonParameters</span></span>
<span data-ttu-id="f2dad-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2dad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2dad-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2dad-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2dad-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2dad-135">INPUTS</span></span>

## <span data-ttu-id="f2dad-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2dad-136">OUTPUTS</span></span>

### <span data-ttu-id="f2dad-137">Microsoft. Windowsazme. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="f2dad-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="f2dad-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2dad-138">NOTES</span></span>

## <span data-ttu-id="f2dad-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2dad-139">RELATED LINKS</span></span>

[<span data-ttu-id="f2dad-140">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="f2dad-140">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)


