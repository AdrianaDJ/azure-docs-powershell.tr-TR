---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105537"
---
# <span data-ttu-id="4c741-101">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="4c741-101">Get-AzureSubscription</span></span>

## <span data-ttu-id="4c741-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c741-102">SYNOPSIS</span></span>
<span data-ttu-id="4c741-103">Azure hesabındaki Azure aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-103">Gets  Azure subscriptions in Azure account.</span></span>

## <span data-ttu-id="4c741-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c741-104">SYNTAX</span></span>

### <span data-ttu-id="4c741-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c741-105">ByName (Default)</span></span>
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c741-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="4c741-106">ById</span></span>
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c741-107">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="4c741-107">Default</span></span>
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4c741-108">Son</span><span class="sxs-lookup"><span data-stu-id="4c741-108">Current</span></span>
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4c741-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c741-109">DESCRIPTION</span></span>
<span data-ttu-id="4c741-110">**Get-azuyeniden gönderme Scription** cmdlet 'i Azure hesabınızdaki abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-110">The **Get-AzureSubscription** cmdlet gets the subscriptions in your Azure account.</span></span>
<span data-ttu-id="4c741-111">Bu cmdlet 'i abonelik hakkında bilgi almak ve aboneliği diğer cmdlet 'lere boru yapmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c741-111">You can use this cmdlet to get information about the subscription and to pipe the subscription to other cmdlets.</span></span>

<span data-ttu-id="4c741-112">**Get-azuyeniden gönderme betikte** Azure hesaplarınıza erişim gerekir.</span><span class="sxs-lookup"><span data-stu-id="4c741-112">**Get-AzureSubscription** requires access to your Azure accounts.</span></span>
<span data-ttu-id="4c741-113">**Get-Azuyeniden gönderme komut** **dosyasına başlamadan** önce, **Add-AzureAccount** cmdlet 'Ini veya yayımlama ayarları dosyasını ( **Get-azuyeniden yayımdosyası**</span><span class="sxs-lookup"><span data-stu-id="4c741-113">Before you run **Get-AzureSubscription** , you must run the **Add-AzureAccount** cmdlet or the cmdlets that download and install a publish settings file ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span></span>

<span data-ttu-id="4c741-114">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4c741-114">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4c741-115">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4c741-115">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="4c741-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c741-116">EXAMPLES</span></span>

### <span data-ttu-id="4c741-117">Örnek 1: tüm abonelikleri al</span><span class="sxs-lookup"><span data-stu-id="4c741-117">Example 1: Get all subscriptions</span></span>
```
C:\PS>Get-AzureSubscription
```

<span data-ttu-id="4c741-118">Bu komut, hesaptaki tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-118">This command gets all subscriptions in the account.</span></span>

### <span data-ttu-id="4c741-119">Örnek 2: ada göre abonelik alma</span><span class="sxs-lookup"><span data-stu-id="4c741-119">Example 2: Get a subscription by name</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

<span data-ttu-id="4c741-120">Bu komut yalnızca "MyProdSubsciption" aboneliğini alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-120">This command gets only the "MyProdSubsciption" subscription.</span></span>

### <span data-ttu-id="4c741-121">Örnek 3: varsayılan aboneliği edinin</span><span class="sxs-lookup"><span data-stu-id="4c741-121">Example 3: Get the default subscription</span></span>
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

<span data-ttu-id="4c741-122">Bu komut yalnızca varsayılan aboneliğin adını alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-122">This command gets only the name of the default subscription.</span></span>
<span data-ttu-id="4c741-123">Komut öncelikle aboneliği alır ve ardından aboneliğin **subscriptionName** özelliğini almak için dot yöntemini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4c741-123">The command first gets the subscription and then uses the dot method to get the **SubscriptionName** property of the subscription.</span></span>

### <span data-ttu-id="4c741-124">Örnek 4: seçili abonelik özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="4c741-124">Example 4: Get selected subscription properties</span></span>
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

<span data-ttu-id="4c741-125">Bu komut, geçerli aboneliğin adını ve sertifikasını içeren bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="4c741-125">This command returns a list with the name and certificate of the current subscription.</span></span>
<span data-ttu-id="4c741-126">Geçerli aboneliği almak için **Get-Azuyeniden gönderme** komut dosyası kullanır.</span><span class="sxs-lookup"><span data-stu-id="4c741-126">It uses a **Get-AzureSubscription** command to get the current subscription.</span></span>
<span data-ttu-id="4c741-127">Ardından, aboneliği listedeki seçili özellikleri görüntüleyen **Biçim listesi** komutuna yöneltin.</span><span class="sxs-lookup"><span data-stu-id="4c741-127">Then it pipes the subscription to a **Format-List** command that displays the selected properties in a list.</span></span>

### <span data-ttu-id="4c741-128">Örnek 5: alternatif bir abonelik veri dosyası kullanın</span><span class="sxs-lookup"><span data-stu-id="4c741-128">Example 5: Use an alternate subscription data file</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

<span data-ttu-id="4c741-129">Bu komut, C:\Temp\MySubscriptions.xml aboneliği veri dosyasından abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-129">This command gets subscriptions from  the C:\Temp\MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="4c741-130">**Add-AzureAccount** veya **Import-publishsettingsfile** cmdlet 'lerini çalıştırdığınızda alternatif bir abonelik verileri dosyası belirttiyseniz, **subscriptionveri** dosyası parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4c741-130">Use the **SubscriptionDataFile** parameter if you specified an alternate subscription data file when you ran the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="4c741-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c741-131">PARAMETERS</span></span>

### <span data-ttu-id="4c741-132">-Geçerli</span><span class="sxs-lookup"><span data-stu-id="4c741-132">-Current</span></span>
<span data-ttu-id="4c741-133">Yalnızca geçerli aboneliği (yani, "geçerli" olarak belirlenen aboneliği) alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-133">Gets only the current subscription, that is, the subscription designated as "current."</span></span> <span data-ttu-id="4c741-134">Varsayılan olarak **Get-Azuyeniden gönderme komut** dosyası, Azure hesaplarınızda tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-134">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="4c741-135">Aboneliği "geçerli" olarak belirlemek için, **Select-azuyeniden gönderme scripscripts** cmdlet 'inin **geçerli** parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4c741-135">To designate a subscription as "current," use the **Current** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c741-136">-Varsayılan</span><span class="sxs-lookup"><span data-stu-id="4c741-136">-Default</span></span>
<span data-ttu-id="4c741-137">Yalnızca varsayılan aboneliği (yani, "varsayılan" olarak belirlenen aboneliği) alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-137">Gets only the default subscription, that is, the subscription designated as "default."</span></span> <span data-ttu-id="4c741-138">Varsayılan olarak **Get-Azuyeniden gönderme komut** dosyası, Azure hesaplarınızda tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-138">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="4c741-139">Aboneliği "varsayılan" olarak belirlemek için, **Select-azuyeniden gönderme scripscripts** cmdlet 'inin **varsayılan** parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4c741-139">To designate a subscription as "default," use the **Default** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c741-140">-ExtendedDetails</span><span class="sxs-lookup"><span data-stu-id="4c741-140">-ExtendedDetails</span></span>
<span data-ttu-id="4c741-141">Standart ayarlara ek olarak aboneliğin kota bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4c741-141">Returns quota information for the subscription, in addition to the standard settings.</span></span>

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

### <span data-ttu-id="4c741-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="4c741-142">-Profile</span></span>
<span data-ttu-id="4c741-143">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c741-143">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4c741-144">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4c741-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c741-145">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="4c741-145">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c741-146">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4c741-146">-SubscriptionName</span></span>
<span data-ttu-id="4c741-147">Yalnızca belirtilen aboneliği alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-147">Gets only the specified subscription.</span></span>
<span data-ttu-id="4c741-148">Abonelik adını girin.</span><span class="sxs-lookup"><span data-stu-id="4c741-148">Enter the subscription name.</span></span>
<span data-ttu-id="4c741-149">Değer büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4c741-149">The value is case-sensitive.</span></span>
<span data-ttu-id="4c741-150">Joker karakterler desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="4c741-150">Wildcard characters are not supported.</span></span>
<span data-ttu-id="4c741-151">Varsayılan olarak **Get-Azuyeniden gönderme komut** dosyası, Azure hesaplarınızda tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-151">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c741-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c741-152">CommonParameters</span></span>
<span data-ttu-id="4c741-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c741-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c741-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c741-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c741-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c741-155">INPUTS</span></span>

### <span data-ttu-id="4c741-156">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4c741-156">None</span></span>
<span data-ttu-id="4c741-157">Girişi, **subscriptionName** özelliğine göre değil, ad ile kanal olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c741-157">You can pipe input to the **SubscriptionName** property by name, but not by value.</span></span>

## <span data-ttu-id="4c741-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c741-158">OUTPUTS</span></span>

### <span data-ttu-id="4c741-159">Microsoft. windowsazma. Commands. Utilities. Common. windowsazuyeniden gönderme komutları</span><span class="sxs-lookup"><span data-stu-id="4c741-159">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureSubscription</span></span>

## <span data-ttu-id="4c741-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c741-160">NOTES</span></span>
* <span data-ttu-id="4c741-161">Get-AzureSubscription, **Add-AzureAccount** ve **Import-publishsettingsfile** cmdlet 'lerinin oluşturulduğu abonelik verileri dosyasından verileri alır.</span><span class="sxs-lookup"><span data-stu-id="4c741-161">Get-AzureSubscription gets data from the subscription data file that the **Add-AzureAccount** and **Import-PublishSettingsFile** cmdlets create.</span></span>

## <span data-ttu-id="4c741-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c741-162">RELATED LINKS</span></span>

[<span data-ttu-id="4c741-163">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="4c741-163">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="4c741-164">Get-Azuikinci dosyayı</span><span class="sxs-lookup"><span data-stu-id="4c741-164">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="4c741-165">Import-Azuyeniden yayımlayan ayarları dosyası</span><span class="sxs-lookup"><span data-stu-id="4c741-165">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="4c741-166">Remove-Azuyeniden gönderiliyor</span><span class="sxs-lookup"><span data-stu-id="4c741-166">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="4c741-167">Set-Azuyeniden gönderiliyor</span><span class="sxs-lookup"><span data-stu-id="4c741-167">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


