---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: ABC303ED-8712-4958-B871-E95357012277
online version: ''
schema: 2.0.0
ms.openlocfilehash: 706c1dee2bc4bb21a8cf116d15bfa3e53daeed99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106095"
---
# <span data-ttu-id="754f6-101">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="754f6-101">Remove-AzureSubscription</span></span>

## <span data-ttu-id="754f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="754f6-102">SYNOPSIS</span></span>
<span data-ttu-id="754f6-103">Windows PowerShell 'den bir Azure aboneliğini siler.</span><span class="sxs-lookup"><span data-stu-id="754f6-103">Deletes an Azure subscription from Windows PowerShell.</span></span>

## <span data-ttu-id="754f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="754f6-104">SYNTAX</span></span>

### <span data-ttu-id="754f6-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="754f6-105">Name (Default)</span></span>
```
Remove-AzureSubscription -SubscriptionName <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754f6-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="754f6-106">Id</span></span>
```
Remove-AzureSubscription -SubscriptionId <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="754f6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="754f6-107">DESCRIPTION</span></span>
<span data-ttu-id="754f6-108">**Remove-Azuyeniden gönderme Scription** cmdlet 'i abonelik veri dosyanızdaki bir Azure aboneliğini siler; böylece Windows PowerShell bunu bulamaz.</span><span class="sxs-lookup"><span data-stu-id="754f6-108">The **Remove-AzureSubscription** cmdlet deletes an Azure subscription from your subscription data file so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="754f6-109">Bu cmdlet, Microsoft Azure aboneliğini silmez veya gerçek aboneliği herhangi bir şekilde değiştiremez.</span><span class="sxs-lookup"><span data-stu-id="754f6-109">This cmdlet does not delete the subscription from Microsoft Azure, or change the actual subscription in any way.</span></span>

<span data-ttu-id="754f6-110">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="754f6-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="754f6-111">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="754f6-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="754f6-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="754f6-112">EXAMPLES</span></span>

### <span data-ttu-id="754f6-113">Örnek 1: aboneliği silme</span><span class="sxs-lookup"><span data-stu-id="754f6-113">Example 1: Delete a subscription</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test

Confirm
Are you sure you want to perform this action?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="754f6-114">Bu komut, varsayılan abonelik veri dosyasından "test" aboneliğini siler.</span><span class="sxs-lookup"><span data-stu-id="754f6-114">This command deletes the "Test" subscription from the default subscription data file.</span></span>

### <span data-ttu-id="754f6-115">Örnek 2: alternatif abonelik veri dosyasından silme</span><span class="sxs-lookup"><span data-stu-id="754f6-115">Example 2: Delete from an alternate subscription data file</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test -SubscriptionDataFile C:\Subs\MySubscriptions.xml -Force
```

<span data-ttu-id="754f6-116">Bu komut, MySubscriptions.xml aboneliği veri dosyasından test aboneliğini siler.</span><span class="sxs-lookup"><span data-stu-id="754f6-116">This command deletes the Test subscription from the MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="754f6-117">Komut, onay istemini bastırmak için *Force* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="754f6-117">The command uses the *Force* parameter to suppress the confirmation prompt.</span></span>

### <span data-ttu-id="754f6-118">Örnek 3: betikte aboneliği silme</span><span class="sxs-lookup"><span data-stu-id="754f6-118">Example 3: Delete a subscription in a script</span></span>
```
C:\PS> ...if (Remove-AzureSubscription -SubscriptionName Test -PassThru) {...}
```

<span data-ttu-id="754f6-119">Bu komut, bir **IF** deyiminde **Remove-Azuyeniden posta scripcommand** komutunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="754f6-119">This command uses the **Remove-AzureSubscription** command in an **If** statement.</span></span>
<span data-ttu-id="754f6-120">**Eğer** deyimindeki komut dosyası bloğunun çalıştırılıp içermediğini belirlemek için Boole değeri döndüren *passit* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="754f6-120">It uses the *PassThru* parameter, which returns a Boolean value, to determine whether the script block in the **If** statement is executed.</span></span>

## <span data-ttu-id="754f6-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="754f6-121">PARAMETERS</span></span>

### <span data-ttu-id="754f6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="754f6-122">-Force</span></span>
<span data-ttu-id="754f6-123">Onay istemini bastırır.</span><span class="sxs-lookup"><span data-stu-id="754f6-123">Suppresses the confirmation prompt.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754f6-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="754f6-124">-PassThru</span></span>
<span data-ttu-id="754f6-125">Komut başarılı olduysa $True ve başarısız olursa $False döndürür.</span><span class="sxs-lookup"><span data-stu-id="754f6-125">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="754f6-126">Varsayılan olarak, bu cmdlet hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="754f6-126">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754f6-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="754f6-127">-Profile</span></span>
<span data-ttu-id="754f6-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="754f6-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="754f6-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="754f6-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="754f6-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="754f6-130">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Id
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="754f6-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="754f6-131">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: Name
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="754f6-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="754f6-132">-Confirm</span></span>
<span data-ttu-id="754f6-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="754f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754f6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="754f6-134">-WhatIf</span></span>
<span data-ttu-id="754f6-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="754f6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="754f6-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="754f6-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="754f6-137">CommonParameters</span></span>
<span data-ttu-id="754f6-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="754f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="754f6-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="754f6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="754f6-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="754f6-140">INPUTS</span></span>

### <span data-ttu-id="754f6-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="754f6-141">None</span></span>
<span data-ttu-id="754f6-142">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="754f6-142">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="754f6-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="754f6-143">OUTPUTS</span></span>

### <span data-ttu-id="754f6-144">None veya System. Boolean</span><span class="sxs-lookup"><span data-stu-id="754f6-144">None or System.Boolean</span></span>
<span data-ttu-id="754f6-145">*Passin* parametresini kullanıyorsanız, bu cmdlet bir Boole değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="754f6-145">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="754f6-146">Aksi takdirde hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="754f6-146">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="754f6-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="754f6-147">NOTES</span></span>

## <span data-ttu-id="754f6-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="754f6-148">RELATED LINKS</span></span>

[<span data-ttu-id="754f6-149">Get-Azuyeniden gönderme</span><span class="sxs-lookup"><span data-stu-id="754f6-149">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="754f6-150">Select-Azuyeniden gönderme</span><span class="sxs-lookup"><span data-stu-id="754f6-150">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)

[<span data-ttu-id="754f6-151">Set-Azuyeniden gönderiliyor</span><span class="sxs-lookup"><span data-stu-id="754f6-151">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


