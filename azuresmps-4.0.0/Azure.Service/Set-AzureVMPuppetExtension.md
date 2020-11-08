---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 268D3E91-AB0F-451F-93B2-9226985910B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41648470b76d889c1ee9d47e4200f843e9f11522
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105849"
---
# <span data-ttu-id="ae23f-101">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="ae23f-101">Set-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="ae23f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae23f-102">SYNOPSIS</span></span>
<span data-ttu-id="ae23f-103">Sanal makinenin Pupalı uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ae23f-103">Sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="ae23f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae23f-104">SYNTAX</span></span>

```
Set-AzureVMPuppetExtension [-PuppetMasterServer] <String> [[-Version] <String>] [-Disable]
 [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ae23f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae23f-105">DESCRIPTION</span></span>
<span data-ttu-id="ae23f-106">**Set-AzureVMPuppetExtension** cmdlet 'i sanal makinenin Pupevcil hayvan uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ae23f-106">The **Set-AzureVMPuppetExtension** cmdlet sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="ae23f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae23f-107">EXAMPLES</span></span>

### <span data-ttu-id="ae23f-108">Örnek 1: sanal makine için Pupevcil hayvan uzantısını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ae23f-108">Example 1: Set the Puppet extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="ae23f-109">Bu örnekte, belirtilen sanal makinenin Pupevcil hayvan uzantısı $VM değişken olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ae23f-109">This example sets the Puppet extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="ae23f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae23f-110">PARAMETERS</span></span>

### <span data-ttu-id="ae23f-111">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="ae23f-111">-Disable</span></span>
<span data-ttu-id="ae23f-112">Bu cmdlet 'in uzantı durumunu devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae23f-112">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae23f-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ae23f-113">-InformationAction</span></span>
<span data-ttu-id="ae23f-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae23f-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ae23f-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ae23f-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae23f-116">'A</span><span class="sxs-lookup"><span data-stu-id="ae23f-116">Continue</span></span>
- <span data-ttu-id="ae23f-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="ae23f-117">Ignore</span></span>
- <span data-ttu-id="ae23f-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="ae23f-118">Inquire</span></span>
- <span data-ttu-id="ae23f-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="ae23f-119">SilentlyContinue</span></span>
- <span data-ttu-id="ae23f-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="ae23f-120">Stop</span></span>
- <span data-ttu-id="ae23f-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="ae23f-121">Suspend</span></span>

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

### <span data-ttu-id="ae23f-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="ae23f-122">-InformationVariable</span></span>
<span data-ttu-id="ae23f-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae23f-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ae23f-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="ae23f-124">-Profile</span></span>
<span data-ttu-id="ae23f-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae23f-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae23f-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ae23f-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae23f-127">-PuppetMasterServer</span><span class="sxs-lookup"><span data-stu-id="ae23f-127">-PuppetMasterServer</span></span>
<span data-ttu-id="ae23f-128">Pupalı ana sunucusunun tam etki alanı adını (FQDN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae23f-128">Specifies the fully qualified domain name (FQDN) of puppet master server.</span></span>

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

### <span data-ttu-id="ae23f-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="ae23f-129">-ReferenceName</span></span>
<span data-ttu-id="ae23f-130">Uzantının başvuru adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae23f-130">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="ae23f-131">Bu, uzantıya başvurmak için kullanılan Kullanıcı tanımlı bir dizedir.</span><span class="sxs-lookup"><span data-stu-id="ae23f-131">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="ae23f-132">Uzantı sanal makineye ilk kez eklendiğinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="ae23f-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="ae23f-133">Sonraki güncelleştirmelerde, uzantıyı güncelleştirdiğinizde önceden kullanılmış olan başvuru adını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ae23f-133">For subsequent updates, you need to specify the previously used reference name when you update the extension.</span></span>
<span data-ttu-id="ae23f-134">Uzantıya atanan ReferenceName, **Get-AzureVM** cmdlet 'i kullanılarak döndürülür.</span><span class="sxs-lookup"><span data-stu-id="ae23f-134">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae23f-135">-Version</span><span class="sxs-lookup"><span data-stu-id="ae23f-135">-Version</span></span>
<span data-ttu-id="ae23f-136">Uzantı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae23f-136">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae23f-137">-VM</span><span class="sxs-lookup"><span data-stu-id="ae23f-137">-VM</span></span>
<span data-ttu-id="ae23f-138">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae23f-138">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="ae23f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae23f-139">CommonParameters</span></span>
<span data-ttu-id="ae23f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae23f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae23f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae23f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae23f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae23f-142">INPUTS</span></span>

## <span data-ttu-id="ae23f-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae23f-143">OUTPUTS</span></span>

## <span data-ttu-id="ae23f-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae23f-144">NOTES</span></span>

## <span data-ttu-id="ae23f-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae23f-145">RELATED LINKS</span></span>

[<span data-ttu-id="ae23f-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ae23f-146">Get-AzureVM</span></span>](./Get-AzureVM.md)


