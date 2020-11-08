---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106255"
---
# <span data-ttu-id="b9126-101">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b9126-101">Import-AzureVM</span></span>

## <span data-ttu-id="b9126-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9126-102">SYNOPSIS</span></span>
<span data-ttu-id="b9126-103">Bir dosyadan Azure sanal makine durumunu içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="b9126-103">Imports an Azure virtual machine state from a file.</span></span>

## <span data-ttu-id="b9126-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9126-104">SYNTAX</span></span>

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9126-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9126-105">DESCRIPTION</span></span>
<span data-ttu-id="b9126-106">**Import-AzureVM** cmdlet 'ı bir XML dosyasından sanal makinenin önceden kaydedilmiş durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="b9126-106">The **Import-AzureVM** cmdlet imports the previously saved state of a virtual machine from an XML file.</span></span>
<span data-ttu-id="b9126-107">Bu cmdlet, içeri aktarılan verilerden bir sanal makine oluşturmak istediğinizde kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="b9126-107">This cmdlet is useful when you want to subsequently create a virtual machine from the imported data.</span></span>

<span data-ttu-id="b9126-108">**Export-AzureVM** , arkasından **Remove-AzureVM** ve ardından Import- **AzureVM** ' ı çalıştırmak, bir sanal makineyi yeniden oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="b9126-108">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="b9126-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9126-109">EXAMPLES</span></span>

### <span data-ttu-id="b9126-110">Örnek 1: sanal makine durumunu Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="b9126-110">Example 1: Import a virtual machine state</span></span>
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

<span data-ttu-id="b9126-111">Bu komut VMstate.xml dosyasından bir sanal makinenin durumunu alır ve belirtilen bulut hizmetinde sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b9126-111">This command imports the state of a virtual machine from the VMstate.xml file, and then creates a virtual machine in the specified cloud service.</span></span>

## <span data-ttu-id="b9126-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9126-112">PARAMETERS</span></span>

### <span data-ttu-id="b9126-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b9126-113">-InformationAction</span></span>
<span data-ttu-id="b9126-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9126-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b9126-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b9126-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b9126-116">'A</span><span class="sxs-lookup"><span data-stu-id="b9126-116">Continue</span></span>
- <span data-ttu-id="b9126-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="b9126-117">Ignore</span></span>
- <span data-ttu-id="b9126-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="b9126-118">Inquire</span></span>
- <span data-ttu-id="b9126-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="b9126-119">SilentlyContinue</span></span>
- <span data-ttu-id="b9126-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="b9126-120">Stop</span></span>
- <span data-ttu-id="b9126-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="b9126-121">Suspend</span></span>

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

### <span data-ttu-id="b9126-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="b9126-122">-InformationVariable</span></span>
<span data-ttu-id="b9126-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9126-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b9126-124">-Yol</span><span class="sxs-lookup"><span data-stu-id="b9126-124">-Path</span></span>
<span data-ttu-id="b9126-125">Önceden kaydedilmiş sanal makine durumunu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9126-125">Specifies the path of the file with the previously saved virtual machine state.</span></span>

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

### <span data-ttu-id="b9126-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9126-126">CommonParameters</span></span>
<span data-ttu-id="b9126-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9126-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9126-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9126-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9126-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9126-129">INPUTS</span></span>

## <span data-ttu-id="b9126-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9126-130">OUTPUTS</span></span>

## <span data-ttu-id="b9126-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9126-131">NOTES</span></span>

## <span data-ttu-id="b9126-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9126-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9126-133">Dışarı aktarma-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b9126-133">Export-AzureVM</span></span>](./Export-AzureVM.md)

[<span data-ttu-id="b9126-134">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b9126-134">New-AzureVM</span></span>](./New-AzureVM.md)


