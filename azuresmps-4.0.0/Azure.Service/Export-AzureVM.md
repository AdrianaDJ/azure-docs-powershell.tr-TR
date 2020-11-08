---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 78099E89-63C9-4019-A4ED-EF37D2383A09
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23e6165e50c227320875fa70e97d63b0cdd78781
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105677"
---
# <span data-ttu-id="697f0-101">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="697f0-101">Export-AzureVM</span></span>

## <span data-ttu-id="697f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="697f0-102">SYNOPSIS</span></span>
<span data-ttu-id="697f0-103">Bir Azure sanal makine durumunu dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="697f0-103">Exports an Azure virtual machine state to a file.</span></span>

## <span data-ttu-id="697f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="697f0-104">SYNTAX</span></span>

```
Export-AzureVM [-ServiceName] <String> [-Name] <String> [-Path] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="697f0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="697f0-105">DESCRIPTION</span></span>
<span data-ttu-id="697f0-106">**Export-AzureVM** cmdlet 'i bir sanal makinenin durumunu. xml dosyasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="697f0-106">The **Export-AzureVM** cmdlet exports the state of a virtual machine to an .xml file.</span></span>

<span data-ttu-id="697f0-107">**Export-AzureVM** , arkasından **Remove-AzureVM** ve ardından Import- **AzureVM** ' ı çalıştırmak, bir sanal makineyi yeniden oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="697f0-107">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="697f0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="697f0-108">EXAMPLES</span></span>

### <span data-ttu-id="697f0-109">Örnek 1: sanal makineyi dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="697f0-109">Example 1: Export a virtual machine</span></span>
```
PS C:\> Export-AzureVM -ServiceName "ContosoService" -Name "ContosoRole06" -Path "C:\vms\VMstate.xml"
```

<span data-ttu-id="697f0-110">Bu komut belirtilen sanal makinenin durumunu VMstate.xml dosyasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="697f0-110">This command exports the state of the specified virtual machine to the VMstate.xml file.</span></span>

## <span data-ttu-id="697f0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="697f0-111">PARAMETERS</span></span>

### <span data-ttu-id="697f0-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="697f0-112">-InformationAction</span></span>
<span data-ttu-id="697f0-113">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="697f0-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="697f0-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="697f0-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="697f0-115">'A</span><span class="sxs-lookup"><span data-stu-id="697f0-115">Continue</span></span>
- <span data-ttu-id="697f0-116">Manıza</span><span class="sxs-lookup"><span data-stu-id="697f0-116">Ignore</span></span>
- <span data-ttu-id="697f0-117">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="697f0-117">Inquire</span></span>
- <span data-ttu-id="697f0-118">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="697f0-118">SilentlyContinue</span></span>
- <span data-ttu-id="697f0-119">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="697f0-119">Stop</span></span>
- <span data-ttu-id="697f0-120">Biliriz</span><span class="sxs-lookup"><span data-stu-id="697f0-120">Suspend</span></span>

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

### <span data-ttu-id="697f0-121">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="697f0-121">-InformationVariable</span></span>
<span data-ttu-id="697f0-122">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="697f0-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="697f0-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="697f0-123">-Name</span></span>
<span data-ttu-id="697f0-124">Bu cmdlet 'in durumu dışarı aktardığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="697f0-124">Specifies the name of the virtual machine for which this cmdlet exports state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="697f0-125">-Yol</span><span class="sxs-lookup"><span data-stu-id="697f0-125">-Path</span></span>
<span data-ttu-id="697f0-126">Bu cmdlet 'in sanal makine durumunu kaydettiği yolu ve dosya adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="697f0-126">Specifies the path and file name to which this cmdlet saves the virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="697f0-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="697f0-127">-Profile</span></span>
<span data-ttu-id="697f0-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="697f0-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="697f0-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="697f0-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="697f0-130">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="697f0-130">-ServiceName</span></span>
<span data-ttu-id="697f0-131">Sanal makineyi barındıran Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="697f0-131">Specifies the name of the Azure service that hosts the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="697f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="697f0-132">CommonParameters</span></span>
<span data-ttu-id="697f0-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="697f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="697f0-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="697f0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="697f0-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="697f0-135">INPUTS</span></span>

## <span data-ttu-id="697f0-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="697f0-136">OUTPUTS</span></span>

## <span data-ttu-id="697f0-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="697f0-137">NOTES</span></span>

## <span data-ttu-id="697f0-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="697f0-138">RELATED LINKS</span></span>

[<span data-ttu-id="697f0-139">İçeri aktarma-AzureVM</span><span class="sxs-lookup"><span data-stu-id="697f0-139">Import-AzureVM</span></span>](./Import-AzureVM.md)


