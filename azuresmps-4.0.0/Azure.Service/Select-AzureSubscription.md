---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105445"
---
# <span data-ttu-id="83b6c-101">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="83b6c-101">Select-AzureSubscription</span></span>

## <span data-ttu-id="83b6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="83b6c-103">Geçerli ve varsayılan Azure aboneliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="83b6c-103">Changes the current and default Azure subscriptions.</span></span>

## <span data-ttu-id="83b6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83b6c-104">SYNTAX</span></span>

### <span data-ttu-id="83b6c-105">SelectSubscriptionByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="83b6c-105">SelectSubscriptionByNameParameterSet (Default)</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="83b6c-106">SelectDefaultSubscriptionByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="83b6c-106">SelectDefaultSubscriptionByNameParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="83b6c-107">Select Subscriptionbyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="83b6c-107">SelectSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="83b6c-108">Selectdefaultsubscriptionbyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="83b6c-108">SelectDefaultSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="83b6c-109">NoCurrentSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="83b6c-109">NoCurrentSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="83b6c-110">NoDefaultSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="83b6c-110">NoDefaultSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="83b6c-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="83b6c-111">DESCRIPTION</span></span>
<span data-ttu-id="83b6c-112">**Select-azuyeniden gönderme Scription** cmdlet 'i geçerli ve varsayılan Azure aboneliklerini ayarlar ve temizler.</span><span class="sxs-lookup"><span data-stu-id="83b6c-112">The **Select-AzureSubscription** cmdlet sets and clears the current and default Azure subscriptions.</span></span>

<span data-ttu-id="83b6c-113">"Geçerli abonelik", geçerli Windows PowerShell oturumunda varsayılan olarak kullanılan aboneliğiniz.</span><span class="sxs-lookup"><span data-stu-id="83b6c-113">The "current subscription" is the subscription that is used by default in the current Windows PowerShell session.</span></span>
<span data-ttu-id="83b6c-114">Varsayılan olarak "varsayılan abonelik" tüm Windows PowerShell oturumlarında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="83b6c-114">The "default subscription" is used by default in all Windows PowerShell sessions.</span></span>
<span data-ttu-id="83b6c-115">"Geçerli abonelik" etiketi, diğer tüm oturumlarda "varsayılan abonelik" değiştirilmeden geçerli oturumda varsayılan olarak kullanılacak farklı bir abonelik belirtmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="83b6c-115">The "current subscription" label lets you specify a different subscription to be used by default for the current session without changing the "default subscription" for all other sessions.</span></span>

<span data-ttu-id="83b6c-116">"Varsayılan" abonelik ataması, abonelik veri dosyanıza kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="83b6c-116">The "default" subscription designation is saved in your subscription data file.</span></span>
<span data-ttu-id="83b6c-117">Oturuma özgü "geçerli" ataması kaydedilmez.</span><span class="sxs-lookup"><span data-stu-id="83b6c-117">The session-specific "current" designation is not saved.</span></span>

<span data-ttu-id="83b6c-118">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="83b6c-118">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="83b6c-119">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="83b6c-119">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="83b6c-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83b6c-120">EXAMPLES</span></span>

### <span data-ttu-id="83b6c-121">Örnek 1: geçerli aboneliği ayarlama</span><span class="sxs-lookup"><span data-stu-id="83b6c-121">Example 1: Set the current subscription</span></span>
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

<span data-ttu-id="83b6c-122">Bu komut, geçerli aboneliği "ContosoEngineering" yapar.</span><span class="sxs-lookup"><span data-stu-id="83b6c-122">This command makes "ContosoEngineering" the current subscription.</span></span>

### <span data-ttu-id="83b6c-123">Örnek 2: varsayılan aboneliği ayarlama</span><span class="sxs-lookup"><span data-stu-id="83b6c-123">Example 2: Set the default subscription</span></span>
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

<span data-ttu-id="83b6c-124">Bu komut varsayılan aboneliği "ContosoFinance" olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="83b6c-124">This command changes the default subscription to "ContosoFinance."</span></span> <span data-ttu-id="83b6c-125">Varsayılan abonelik verileri dosyası yerine Subscriptions.xml aboneliği veri dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="83b6c-125">It saves the setting in the Subscriptions.xml subscription data file, instead of the default subscription data file.</span></span>

## <span data-ttu-id="83b6c-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83b6c-126">PARAMETERS</span></span>

### <span data-ttu-id="83b6c-127">-Hesap</span><span class="sxs-lookup"><span data-stu-id="83b6c-127">-Account</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b6c-128">-Geçerli</span><span class="sxs-lookup"><span data-stu-id="83b6c-128">-Current</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b6c-129">-Varsayılan</span><span class="sxs-lookup"><span data-stu-id="83b6c-129">-Default</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b6c-130">-NoCurrent</span><span class="sxs-lookup"><span data-stu-id="83b6c-130">-NoCurrent</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b6c-131">-NoDefault</span><span class="sxs-lookup"><span data-stu-id="83b6c-131">-NoDefault</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b6c-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="83b6c-132">-PassThru</span></span>
<span data-ttu-id="83b6c-133">Komut başarılı olduysa $True ve başarısız olursa $False döndürür.</span><span class="sxs-lookup"><span data-stu-id="83b6c-133">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="83b6c-134">Varsayılan olarak, bu cmdlet hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="83b6c-134">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="83b6c-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="83b6c-135">-Profile</span></span>
<span data-ttu-id="83b6c-136">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="83b6c-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="83b6c-137">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="83b6c-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83b6c-138">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="83b6c-138">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b6c-139">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="83b6c-139">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b6c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b6c-140">CommonParameters</span></span>
<span data-ttu-id="83b6c-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83b6c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b6c-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b6c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b6c-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83b6c-143">INPUTS</span></span>

### <span data-ttu-id="83b6c-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="83b6c-144">None</span></span>
<span data-ttu-id="83b6c-145">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="83b6c-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="83b6c-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83b6c-146">OUTPUTS</span></span>

### <span data-ttu-id="83b6c-147">None veya System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83b6c-147">None or System.Boolean</span></span>
<span data-ttu-id="83b6c-148">*Passin* parametresini kullanıyorsanız, bu cmdlet bir Boole değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="83b6c-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="83b6c-149">Varsayılan olarak, hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="83b6c-149">By default, it does not generate any output.</span></span>

## <span data-ttu-id="83b6c-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83b6c-150">NOTES</span></span>

## <span data-ttu-id="83b6c-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83b6c-151">RELATED LINKS</span></span>

[<span data-ttu-id="83b6c-152">Get-Azuyeniden gönderme</span><span class="sxs-lookup"><span data-stu-id="83b6c-152">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="83b6c-153">Remove-Azuyeniden gönderiliyor</span><span class="sxs-lookup"><span data-stu-id="83b6c-153">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="83b6c-154">Set-Azuyeniden gönderiliyor</span><span class="sxs-lookup"><span data-stu-id="83b6c-154">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


