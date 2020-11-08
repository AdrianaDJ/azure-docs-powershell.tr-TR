---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105870"
---
# <span data-ttu-id="a31f0-101">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="a31f0-101">Remove-AzureAccount</span></span>

## <span data-ttu-id="a31f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a31f0-102">SYNOPSIS</span></span>
<span data-ttu-id="a31f0-103">Windows PowerShell 'den bir Azure hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="a31f0-103">Deletes an Azure account from Windows PowerShell.</span></span>

## <span data-ttu-id="a31f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a31f0-104">SYNTAX</span></span>

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a31f0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a31f0-105">DESCRIPTION</span></span>
<span data-ttu-id="a31f0-106">**Remove-AzureAccount** cmdlet 'i, gezici kullanıcı profilinizdeki abonelik verileri dosyasındaki bir Azure hesabını ve aboneliğini siler.</span><span class="sxs-lookup"><span data-stu-id="a31f0-106">The **Remove-AzureAccount** cmdlet deletes an Azure account and its subscriptions from the subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="a31f0-107">Hesabı Microsoft Azure 'dan silmez veya fiili hesabı hiçbir şekilde değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="a31f0-107">It does not delete the account from Microsoft Azure, or change the actual account in any way.</span></span>

<span data-ttu-id="a31f0-108">Bu cmdlet 'i kullanmak, Azure hesabınızda oturum açmak gibi çok kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="a31f0-108">Using this cmdlet is a lot like logging out of your Azure account.</span></span>
<span data-ttu-id="a31f0-109">Ve hesapta yeniden oturum açmak istiyorsanız, **Add-AzureAccount** veya **Import-Azuyeniden yayımlayan ayarları dosyasını** kullanarak hesabı Windows PowerShell 'e yeniden ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a31f0-109">And, if you want to log into the account again, use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** to add the account to Windows PowerShell again.</span></span>

<span data-ttu-id="a31f0-110">Ayrıca **Remove-AzureAccount** cmdlet 'ini kullanarak Azure PowerShell cmdlet 'lerinin Azure hesabınızda oturum açma şeklini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a31f0-110">You can also use **Remove-AzureAccount** cmdlet to change the way the Azure PowerShell cmdlets sign into your Azure account.</span></span>
<span data-ttu-id="a31f0-111">Hesabınızda hem **Import-azubir yeniden yayımcıya** da **Add-AzureAccount** ' a ait bir yönetim sertifikası varsa, Azure PowerShell cmdlet 'leri yalnızca erişim belirtecini kullanır; yönetim sertifikasını yoksayar.</span><span class="sxs-lookup"><span data-stu-id="a31f0-111">If your account has both a management certificate from **Import-AzurePublishSettingsFile** and an access token from **Add-AzureAccount** , the Azure PowerShell cmdlets use only the access token; they ignore the management certificate.</span></span>
<span data-ttu-id="a31f0-112">Yönetim sertifikasını kullanmak için, **Remove-AzureAccount** ' ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="a31f0-112">To use the management certificate, run **Remove-AzureAccount**.</span></span>
<span data-ttu-id="a31f0-113">**Remove-AzureAccount** hem yönetim sertifikasını hem de bir erişim belirtecini bulduğunda, hesabı silmek yerine yalnızca erişim belirtecini siler.</span><span class="sxs-lookup"><span data-stu-id="a31f0-113">When **Remove-AzureAccount** finds both a management certificate and an access token, it deletes only the access token, instead of deleting the account.</span></span>
<span data-ttu-id="a31f0-114">Yönetim sertifikası hala orada olduğundan hesap yine Windows PowerShell için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a31f0-114">The management certificate is still there, so account is still available to Windows PowerShell.</span></span>

<span data-ttu-id="a31f0-115">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a31f0-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a31f0-116">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a31f0-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="a31f0-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a31f0-117">EXAMPLES</span></span>

### <span data-ttu-id="a31f0-118">Örnek 1: hesap kaldırma</span><span class="sxs-lookup"><span data-stu-id="a31f0-118">Example 1: Remove an account</span></span>
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

<span data-ttu-id="a31f0-119">Bu komut, admin@contoso.com abonelik veri dosyanızı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a31f0-119">This command removes the admin@contoso.com from your subscription data file.</span></span>
<span data-ttu-id="a31f0-120">Komut tamamlandığında, hesap artık Windows PowerShell tarafından kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="a31f0-120">When the command completes, the account is no longer available to Windows PowerShell.</span></span>

## <span data-ttu-id="a31f0-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a31f0-121">PARAMETERS</span></span>

### <span data-ttu-id="a31f0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a31f0-122">-Force</span></span>
<span data-ttu-id="a31f0-123">Onay istemini bastırır.</span><span class="sxs-lookup"><span data-stu-id="a31f0-123">Suppresses the confirmation prompt.</span></span>
<span data-ttu-id="a31f0-124">Varsayılan olarak, **Remove-AzureAccount** , hesabı Windows PowerShell 'den kaldırmadan önce sorar.</span><span class="sxs-lookup"><span data-stu-id="a31f0-124">By default, **Remove-AzureAccount** prompts you before removing the account from Windows PowerShell.</span></span>

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

### <span data-ttu-id="a31f0-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="a31f0-125">-Name</span></span>
<span data-ttu-id="a31f0-126">Kaldırılacak hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a31f0-126">Specifies the name of the account to remove.</span></span>
<span data-ttu-id="a31f0-127">Parametre değeri büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="a31f0-127">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="a31f0-128">Joker karakterler desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="a31f0-128">Wildcard characters are not supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31f0-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a31f0-129">-PassThru</span></span>
<span data-ttu-id="a31f0-130">Komut başarılı olduysa $True ve başarısız olursa $False döndürür.</span><span class="sxs-lookup"><span data-stu-id="a31f0-130">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="a31f0-131">Varsayılan olarak, bu cmdlet hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="a31f0-131">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="a31f0-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="a31f0-132">-Profile</span></span>
<span data-ttu-id="a31f0-133">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a31f0-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a31f0-134">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a31f0-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a31f0-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="a31f0-135">-Confirm</span></span>
<span data-ttu-id="a31f0-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a31f0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a31f0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a31f0-137">-WhatIf</span></span>
<span data-ttu-id="a31f0-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a31f0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a31f0-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a31f0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a31f0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31f0-140">CommonParameters</span></span>
<span data-ttu-id="a31f0-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a31f0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31f0-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31f0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31f0-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a31f0-143">INPUTS</span></span>

### <span data-ttu-id="a31f0-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a31f0-144">None</span></span>
<span data-ttu-id="a31f0-145">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a31f0-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a31f0-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a31f0-146">OUTPUTS</span></span>

### <span data-ttu-id="a31f0-147">None veya System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a31f0-147">None or System.Boolean</span></span>
<span data-ttu-id="a31f0-148">*Passin* parametresini kullanıyorsanız, bu cmdlet bir Boole değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="a31f0-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="a31f0-149">Aksi takdirde hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="a31f0-149">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="a31f0-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a31f0-150">NOTES</span></span>

## <span data-ttu-id="a31f0-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a31f0-151">RELATED LINKS</span></span>

[<span data-ttu-id="a31f0-152">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="a31f0-152">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="a31f0-153">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="a31f0-153">Get-AzureAccount</span></span>](./Get-AzureAccount.md)


