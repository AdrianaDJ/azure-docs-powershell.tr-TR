---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105633"
---
# <span data-ttu-id="e0c93-101">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e0c93-101">Get-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="e0c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0c93-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c93-103">Azure aboneliği için yayımlama ayarları dosyasını indirir.</span><span class="sxs-lookup"><span data-stu-id="e0c93-103">Downloads the publish settings file for an Azure subscription.</span></span>

## <span data-ttu-id="e0c93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0c93-104">SYNTAX</span></span>

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0c93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0c93-105">DESCRIPTION</span></span>
<span data-ttu-id="e0c93-106">**Get-Azuikinci dosyayı** ayarlar cmdlet 'i, hesabınızdaki bir aboneliğin yayımlama ayarları dosyasını indirir.</span><span class="sxs-lookup"><span data-stu-id="e0c93-106">The **Get-AzurePublishSettingsFile** cmdlet downloads a publish settings file for a subscription in your account.</span></span>
<span data-ttu-id="e0c93-107">Komut tamamlandığında, dosyadaki ayarların Windows PowerShell tarafından kullanılabilmesini sağlamak için **Import-PublishSettingsFile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e0c93-107">When the command completes, you can use the **Import-PublishSettingsFile** cmdlet to make the settings in the file available to Windows PowerShell.</span></span>

<span data-ttu-id="e0c93-108">Azure hesabınızı Windows PowerShell 'in kullanımına sunmak için, bir yayımlama ayarları dosyası veya **Add-AzureAccount** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e0c93-108">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="e0c93-109">Yayımlama ayarları dosyaları oturumu önceden hazırlamanıza olanak tanır; böylece komut dosyalarını ve arka plan işlerini katılımsız olarak çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e0c93-109">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="e0c93-110">Ancak, tüm hizmetler yayımlama ayarları dosyalarını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="e0c93-110">However, not all services support publish settings files.</span></span>
<span data-ttu-id="e0c93-111">Örneğin, **AzureResourceManager** modülü yayımlama ayarları dosyalarını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="e0c93-111">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="e0c93-112">**Get-azuyeniden yayımlamadan önce Settings dosyasını** çalıştırdığınızda, varsayılan tarayıcınızı açar ve Azure hesabınızda oturum açmanızı ister ve yayımlama ayarları dosyası için bir dosya sistemi konumu seçin.</span><span class="sxs-lookup"><span data-stu-id="e0c93-112">When you run **Get-AzurePublishSettingsFile** , it opens your default browser and prompts you to sign into your Azure account, select a subscription, and select a file system location for the publish settings file.</span></span>
<span data-ttu-id="e0c93-113">Ardından, aboneliğiniz için yayımlama ayarları dosyasını seçtiğiniz dosyaya yükler.</span><span class="sxs-lookup"><span data-stu-id="e0c93-113">Then, it downloads the publish settings file for your subscription into the file that you selected.</span></span>

<span data-ttu-id="e0c93-114">"Yayımlama ayarları dosyası". publishsettings dosya adı uzantısına sahip bir XML dosyasıdır.</span><span class="sxs-lookup"><span data-stu-id="e0c93-114">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span>
<span data-ttu-id="e0c93-115">Dosya, Azure abonelikleriniz için yönetim kimlik bilgilerini sağlayan kodlanmış bir sertifika içeriyor.</span><span class="sxs-lookup"><span data-stu-id="e0c93-115">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span>

<span data-ttu-id="e0c93-116">**Güvenlik notu:** Yayımlama ayarları dosyaları, Azure aboneliğinizi ve hizmetlerinizi yönetmek için kullanılan kimlik bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="e0c93-116">**Security Note:** Publish settings files contains credentials that are used to administer your Azure subscriptions and services.</span></span>
<span data-ttu-id="e0c93-117">Kötü niyetli kullanıcılar yayımlama ayarları dosyanıza erişlerse, Azure hizmetlerini düzenleyebilir, oluşturabilir ve silebilir.</span><span class="sxs-lookup"><span data-stu-id="e0c93-117">If  malicious users access your publish settings file,  they can edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="e0c93-118">En iyi güvenlik uygulaması olarak, dosyayı Indirmeler veya belgeler klasörünüzdeki bir konuma kaydedin ve sonra da ayarları içeri aktarmak için **import-azudandanayardandosya** cmdlet 'ini kullandıktan sonra silin.</span><span class="sxs-lookup"><span data-stu-id="e0c93-118">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

<span data-ttu-id="e0c93-119">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e0c93-119">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e0c93-120">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e0c93-120">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="e0c93-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0c93-121">EXAMPLES</span></span>

### <span data-ttu-id="e0c93-122">Örnek 1: yayımlama ayarları dosyasını Indirme</span><span class="sxs-lookup"><span data-stu-id="e0c93-122">Example 1: Download a publish settings file</span></span>
```
PS C:\> Get-AzurePublishSettingsFile
```

<span data-ttu-id="e0c93-123">Bu komut varsayılan tarayıcınızı açar, Windows Azure hesabınıza bağlanır ve ardından hesabınızın. publishsettings dosyasını indirir.</span><span class="sxs-lookup"><span data-stu-id="e0c93-123">This command opens your default browser, connects to your Windows Azure account, and then downloads the .publishsettings file for your account.</span></span>

### <span data-ttu-id="e0c93-124">Örnek 2: bölge belirtme</span><span class="sxs-lookup"><span data-stu-id="e0c93-124">Example 2: Specify a realm</span></span>
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

<span data-ttu-id="e0c93-125">Bu komut, contoso.com etki alanındaki bir hesabın yayımlama ayarları dosyasını indirir.</span><span class="sxs-lookup"><span data-stu-id="e0c93-125">This command downloads the publish settings file for an account in the contoso.com domain.</span></span>
<span data-ttu-id="e0c93-126">Bir Microsoft hesabı yerine bir kuruluş hesabıyla oturum açtığınızda, **bölge** parametresiyle bir komut kullanın.</span><span class="sxs-lookup"><span data-stu-id="e0c93-126">Use a command with the **Realm** parameter when you sign into Azure with an organizational account, instead of a Microsoft account.</span></span>

## <span data-ttu-id="e0c93-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0c93-127">PARAMETERS</span></span>

### <span data-ttu-id="e0c93-128">-Ortam</span><span class="sxs-lookup"><span data-stu-id="e0c93-128">-Environment</span></span>
<span data-ttu-id="e0c93-129">Bir Azure ortamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0c93-129">Specifies an Azure environment.</span></span>

<span data-ttu-id="e0c93-130">Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="e0c93-130">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="e0c93-131">Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e0c93-131">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="e0c93-132">Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e0c93-132">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="e0c93-133">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e0c93-133">-PassThru</span></span>
<span data-ttu-id="e0c93-134">Komut başarılı olduysa $True ve başarısız olursa $False döndürür.</span><span class="sxs-lookup"><span data-stu-id="e0c93-134">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="e0c93-135">Varsayılan olarak, bu cmdlet hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="e0c93-135">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0c93-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="e0c93-136">-Profile</span></span>
<span data-ttu-id="e0c93-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0c93-137">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e0c93-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e0c93-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0c93-139">-Bölge</span><span class="sxs-lookup"><span data-stu-id="e0c93-139">-Realm</span></span>
<span data-ttu-id="e0c93-140">Kuruluş KIMLIĞINDE kuruluş belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0c93-140">Specifies the organization in an organizational ID.</span></span>
<span data-ttu-id="e0c93-141">Örneğin, Azure 'da oturum açarsanız admin@contoso.com , **bölge** parametresinin değeri contoso.com olur.</span><span class="sxs-lookup"><span data-stu-id="e0c93-141">For example, if you sign into Azure as admin@contoso.com, the value of the **Realm** parameter is contoso.com.</span></span>
<span data-ttu-id="e0c93-142">Azure portalında oturum açmak için kuruluş KIMLIĞI kullandığınızda bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="e0c93-142">Use this parameter when you use an organizational ID to sign into the Azure portal.</span></span>
<span data-ttu-id="e0c93-143">Outlook.com veya live.com hesabı gibi bir Microsoft hesabı kullandığınızda bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="e0c93-143">This parameter is not required when you use a Microsoft account, such as an outlook.com or live.com account.</span></span>

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

### <span data-ttu-id="e0c93-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c93-144">CommonParameters</span></span>
<span data-ttu-id="e0c93-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0c93-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c93-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0c93-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c93-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0c93-147">INPUTS</span></span>

### <span data-ttu-id="e0c93-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e0c93-148">None</span></span>
<span data-ttu-id="e0c93-149">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e0c93-149">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="e0c93-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0c93-150">OUTPUTS</span></span>

### <span data-ttu-id="e0c93-151">None veya System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0c93-151">None or System.Boolean</span></span>
<span data-ttu-id="e0c93-152">*Passin* parametresini kullandığınızda, bu cmdlet bir Boole değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e0c93-152">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="e0c93-153">Aksi halde, bu cmdlet hiçbir çıkış döndürmez</span><span class="sxs-lookup"><span data-stu-id="e0c93-153">Otherwise, this cmdlet does not return any output</span></span>

## <span data-ttu-id="e0c93-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0c93-154">NOTES</span></span>

## <span data-ttu-id="e0c93-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0c93-155">RELATED LINKS</span></span>

[<span data-ttu-id="e0c93-156">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="e0c93-156">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="e0c93-157">Import-Azuyeniden yayımlayan ayarları dosyası</span><span class="sxs-lookup"><span data-stu-id="e0c93-157">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)


