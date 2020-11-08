---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9EA98944-1923-4573-991E-3B9CA21004BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f16b51dc8abf5c6243b4b489789d65029acc3c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106148"
---
# <span data-ttu-id="48a67-101">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="48a67-101">Remove-AzurePublicIP</span></span>

## <span data-ttu-id="48a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48a67-102">SYNOPSIS</span></span>
<span data-ttu-id="48a67-103">Azure sanal makinesinden ortak IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="48a67-103">Removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="48a67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48a67-104">SYNTAX</span></span>

```
Remove-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="48a67-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48a67-105">DESCRIPTION</span></span>
<span data-ttu-id="48a67-106">**Remove-AzurePublicIP** cmdlet 'i Azure sanal MAKINESINDEN ortak IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="48a67-106">The **Remove-AzurePublicIP** cmdlet removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="48a67-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48a67-107">EXAMPLES</span></span>

### <span data-ttu-id="48a67-108">Örnek 1: genel IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="48a67-108">Example 1: Remove Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Remove-AzurePublicIP | Update-AzureVM
```

<span data-ttu-id="48a67-109">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak Ftpınazure adlı hizmette ftpınstance adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="48a67-109">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="48a67-110">Komut, ardışık düzen işlecini kullanarak bu sanal makineyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="48a67-110">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="48a67-111">Geçerli cmdlet, sanal makineden ortak IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="48a67-111">The current cmdlet removes Public IP configuration from the virtual machine.</span></span>
<span data-ttu-id="48a67-112">Komut, sanal makineyi değişikliklerinizi uygulayan **Update-AzureVM** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="48a67-112">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="48a67-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48a67-113">PARAMETERS</span></span>

### <span data-ttu-id="48a67-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="48a67-114">-InformationAction</span></span>
<span data-ttu-id="48a67-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="48a67-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="48a67-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48a67-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48a67-117">'A</span><span class="sxs-lookup"><span data-stu-id="48a67-117">Continue</span></span>
- <span data-ttu-id="48a67-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="48a67-118">Ignore</span></span>
- <span data-ttu-id="48a67-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="48a67-119">Inquire</span></span>
- <span data-ttu-id="48a67-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="48a67-120">SilentlyContinue</span></span>
- <span data-ttu-id="48a67-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="48a67-121">Stop</span></span>
- <span data-ttu-id="48a67-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="48a67-122">Suspend</span></span>

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

### <span data-ttu-id="48a67-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="48a67-123">-InformationVariable</span></span>
<span data-ttu-id="48a67-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="48a67-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="48a67-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="48a67-125">-Profile</span></span>
<span data-ttu-id="48a67-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="48a67-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="48a67-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="48a67-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48a67-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="48a67-128">-PublicIPName</span></span>
<span data-ttu-id="48a67-129">Genel IP adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48a67-129">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a67-130">-VM</span><span class="sxs-lookup"><span data-stu-id="48a67-130">-VM</span></span>
<span data-ttu-id="48a67-131">Bu cmdlet 'in genel IP yapılandırmasını kaldırdıkları sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="48a67-131">Specifies the virtual machine from which this cmdlet removes Public IP configuration.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48a67-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a67-132">CommonParameters</span></span>
<span data-ttu-id="48a67-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48a67-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a67-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48a67-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a67-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48a67-135">INPUTS</span></span>

## <span data-ttu-id="48a67-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48a67-136">OUTPUTS</span></span>

### <span data-ttu-id="48a67-137">Microsoft. Windowsaziy. Commands. ServiceManagement. model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="48a67-137">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="48a67-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48a67-138">NOTES</span></span>

## <span data-ttu-id="48a67-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48a67-139">RELATED LINKS</span></span>

[<span data-ttu-id="48a67-140">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="48a67-140">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="48a67-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="48a67-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="48a67-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="48a67-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)

[<span data-ttu-id="48a67-143">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="48a67-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


