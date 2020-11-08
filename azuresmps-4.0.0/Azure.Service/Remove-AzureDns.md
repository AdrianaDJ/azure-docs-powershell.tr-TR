---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1B1C1459-A602-423D-8CAA-B4901CFC2C82
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f684908e8119da007f8b1f844ebbac40713d51
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106479"
---
# <span data-ttu-id="cf055-101">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="cf055-101">Remove-AzureDns</span></span>

## <span data-ttu-id="cf055-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf055-102">SYNOPSIS</span></span>
<span data-ttu-id="cf055-103">Bir Azure hizmetinden DNS sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cf055-103">Removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="cf055-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf055-104">SYNTAX</span></span>

```
Remove-AzureDns [-Name] <String> [-ServiceName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cf055-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf055-105">DESCRIPTION</span></span>
<span data-ttu-id="cf055-106">**Remove-AzureDns** cmdlet 'i, bir Azure hizmetinden DNS sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cf055-106">The **Remove-AzureDns** cmdlet removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="cf055-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf055-107">EXAMPLES</span></span>

### <span data-ttu-id="cf055-108">Örnek 1: hizmetten DNS sunucusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="cf055-108">Example 1: Remove a DNS server from a service</span></span>
```
PS C:\> Remove-AzureDns -ServiceName "ContosoService" -Name "Dns07"
```

<span data-ttu-id="cf055-109">Bu komut, Dns07 adındaki DNS sunucusunu ContosoService 'ten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cf055-109">This command removes the DNS server named Dns07 from ContosoService.</span></span>

## <span data-ttu-id="cf055-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf055-110">PARAMETERS</span></span>

### <span data-ttu-id="cf055-111">-Force</span><span class="sxs-lookup"><span data-stu-id="cf055-111">-Force</span></span>
<span data-ttu-id="cf055-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="cf055-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf055-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cf055-113">-InformationAction</span></span>
<span data-ttu-id="cf055-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf055-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cf055-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cf055-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cf055-116">'A</span><span class="sxs-lookup"><span data-stu-id="cf055-116">Continue</span></span>
- <span data-ttu-id="cf055-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="cf055-117">Ignore</span></span>
- <span data-ttu-id="cf055-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="cf055-118">Inquire</span></span>
- <span data-ttu-id="cf055-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="cf055-119">SilentlyContinue</span></span>
- <span data-ttu-id="cf055-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="cf055-120">Stop</span></span>
- <span data-ttu-id="cf055-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="cf055-121">Suspend</span></span>

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

### <span data-ttu-id="cf055-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="cf055-122">-InformationVariable</span></span>
<span data-ttu-id="cf055-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf055-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cf055-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="cf055-124">-Name</span></span>
<span data-ttu-id="cf055-125">Bu cmdlet 'in kaldırıldığı DNS sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf055-125">Specifies the name of the DNS server that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cf055-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="cf055-126">-Profile</span></span>
<span data-ttu-id="cf055-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf055-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cf055-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="cf055-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cf055-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="cf055-129">-ServiceName</span></span>
<span data-ttu-id="cf055-130">Bu cmdlet 'in DNS sunucusunu kaldırdığı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf055-130">Specifies the name of the service from which this cmdlet removes a DNS server.</span></span>

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

### <span data-ttu-id="cf055-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf055-131">CommonParameters</span></span>
<span data-ttu-id="cf055-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf055-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf055-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf055-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf055-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf055-134">INPUTS</span></span>

## <span data-ttu-id="cf055-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf055-135">OUTPUTS</span></span>

### <span data-ttu-id="cf055-136">Microsoft. Windowsazme. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="cf055-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="cf055-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf055-137">NOTES</span></span>

## <span data-ttu-id="cf055-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf055-138">RELATED LINKS</span></span>

[<span data-ttu-id="cf055-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="cf055-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="cf055-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="cf055-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="cf055-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="cf055-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="cf055-142">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="cf055-142">Set-AzureDns</span></span>](./Set-AzureDns.md)


