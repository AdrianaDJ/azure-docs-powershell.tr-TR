---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105791"
---
# <span data-ttu-id="656f6-101">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="656f6-101">Set-AzureVMSize</span></span>

## <span data-ttu-id="656f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="656f6-102">SYNOPSIS</span></span>
<span data-ttu-id="656f6-103">Azure sanal makinesinin boyutunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="656f6-103">Sets the size of an Azure virtual machine.</span></span>

## <span data-ttu-id="656f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="656f6-104">SYNTAX</span></span>

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="656f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="656f6-105">DESCRIPTION</span></span>
<span data-ttu-id="656f6-106">**Set-AzureVMSize** cmdlet 'i sanal makinenin boyutunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="656f6-106">The **Set-AzureVMSize** cmdlet updates the size of a virtual machine.</span></span>
<span data-ttu-id="656f6-107">İki parametre vardır: *ınstancesize* , bu sanal makinenin yeni boyutu ve **Get-AzureVM** cmdlet 'i kullanılarak alınan sanal makine nesnesi olan *VM*.</span><span class="sxs-lookup"><span data-stu-id="656f6-107">It has two parameters: *InstanceSize* , which is the new size of the virtual machine, and *VM* , which is a virtual machine object retrieved by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="656f6-108">**Set-AzureVMSize** sonucu **Update-AzureVM** cmdlet 'ine veya daha sonra kullanmak üzere bir değişkende depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="656f6-108">The result of **Set-AzureVMSize** can be piped to the **Update-AzureVM** cmdlet or stored in a variable for later use.</span></span>
<span data-ttu-id="656f6-109">**Update-AzureVM** yürütülmeden fiili değişiklik yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="656f6-109">No actual change is made until **Update-AzureVM** is executed.</span></span>

<span data-ttu-id="656f6-110">Not: Bu cmdlet, sanal makinenin yeniden sağlanmasını gerektirir ve yeni bir IP adresi alabilir.</span><span class="sxs-lookup"><span data-stu-id="656f6-110">Note: This cmdlet will require the virtual machine to be re-provisioned and it might get a new IP address.</span></span>

## <span data-ttu-id="656f6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="656f6-111">EXAMPLES</span></span>

### <span data-ttu-id="656f6-112">Örnek 1: sanal makinenin boyutunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="656f6-112">Example 1: Set the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

<span data-ttu-id="656f6-113">Bu komut, bir sanal makineyi "küçük" boyutunu verecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="656f6-113">This command updates a virtual machine to size "Small".</span></span>

## <span data-ttu-id="656f6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="656f6-114">PARAMETERS</span></span>

### <span data-ttu-id="656f6-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="656f6-115">-InformationAction</span></span>
<span data-ttu-id="656f6-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="656f6-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="656f6-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="656f6-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="656f6-118">'A</span><span class="sxs-lookup"><span data-stu-id="656f6-118">Continue</span></span>
- <span data-ttu-id="656f6-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="656f6-119">Ignore</span></span>
- <span data-ttu-id="656f6-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="656f6-120">Inquire</span></span>
- <span data-ttu-id="656f6-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="656f6-121">SilentlyContinue</span></span>
- <span data-ttu-id="656f6-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="656f6-122">Stop</span></span>
- <span data-ttu-id="656f6-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="656f6-123">Suspend</span></span>

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

### <span data-ttu-id="656f6-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="656f6-124">-InformationVariable</span></span>
<span data-ttu-id="656f6-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="656f6-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="656f6-126">-Instancesize</span><span class="sxs-lookup"><span data-stu-id="656f6-126">-InstanceSize</span></span>
<span data-ttu-id="656f6-127">Sanal makinenin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="656f6-127">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="656f6-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="656f6-128">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="656f6-129">--ExtraSmall--Small--orta--büyük--Extrabüyük--a5--A7</span><span class="sxs-lookup"><span data-stu-id="656f6-129">--ExtraSmall --Small --Medium --Large --ExtraLarge --A5 --A6 --A7</span></span>

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

### <span data-ttu-id="656f6-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="656f6-130">-Profile</span></span>
<span data-ttu-id="656f6-131">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="656f6-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="656f6-132">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="656f6-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="656f6-133">-VM</span><span class="sxs-lookup"><span data-stu-id="656f6-133">-VM</span></span>
<span data-ttu-id="656f6-134">Bu cmdlet 'in boyutu ayarlayan kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="656f6-134">Specifies the persistent virtual machine object that this cmdlet sets the size of.</span></span>

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

### <span data-ttu-id="656f6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="656f6-135">CommonParameters</span></span>
<span data-ttu-id="656f6-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="656f6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="656f6-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="656f6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="656f6-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="656f6-138">INPUTS</span></span>

## <span data-ttu-id="656f6-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="656f6-139">OUTPUTS</span></span>

## <span data-ttu-id="656f6-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="656f6-140">NOTES</span></span>

## <span data-ttu-id="656f6-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="656f6-141">RELATED LINKS</span></span>

[<span data-ttu-id="656f6-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="656f6-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="656f6-143">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="656f6-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


