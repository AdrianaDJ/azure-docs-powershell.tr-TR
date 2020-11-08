---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106261"
---
# <span data-ttu-id="33711-101">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="33711-101">Import-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="33711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33711-102">SYNOPSIS</span></span>
<span data-ttu-id="33711-103">Windows PowerShell 'de Azure hesaplarınızı yönetmenizi sağlayan bir yayımlama ayarları dosyası içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="33711-103">Imports a publish settings file that lets you manage your Azure accounts in Windows PowerShell.</span></span>

## <span data-ttu-id="33711-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33711-104">SYNTAX</span></span>

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="33711-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="33711-105">DESCRIPTION</span></span>
<span data-ttu-id="33711-106">**Import-Azuikinci yeniden yükleyen Settingsfıle** cmdlet 'ı, Azure hesaplarınız hakkında bilgi içeren bir yayımlama ayarları dosyası (\*. publishsettings) içeri aktarır ve bilgisayarınıza bir abonelik verileri dosyası kaydeder.</span><span class="sxs-lookup"><span data-stu-id="33711-106">The **Import-AzurePublishSettingsFile** cmdlet imports a publish settings file (\*.publishsettings) that contains information about your Azure accounts and saves a subscription data file on your computer.</span></span>
<span data-ttu-id="33711-107">Cmdlet tamamlandığında, Azure hesaplarınızı Windows PowerShell 'de yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="33711-107">When the cmdlet completes, you can manage your Azure accounts in Windows PowerShell.</span></span>

<span data-ttu-id="33711-108">**İmport-Azuikinci** kayıt ayarları dosyasını çalıştırmadan önce, yayınlama ayarları dosyasını indiren ve kaydeden **Get-Azu**</span><span class="sxs-lookup"><span data-stu-id="33711-108">Before running **Import-AzurePublishSettingsFile** , run **Get-AzurePublishSettingsFile** , which downloads and saves the publish settings file so you can import it.</span></span>

<span data-ttu-id="33711-109">Azure hesabınızı Windows PowerShell 'in kullanımına sunmak için, bir yayımlama ayarları dosyası veya **Add-AzureAccount** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="33711-109">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="33711-110">Yayımlama ayarları dosyaları oturumu önceden hazırlamanıza olanak tanır; böylece komut dosyalarını ve arka plan işlerini katılımsız olarak çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="33711-110">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="33711-111">Ancak, tüm hizmetler yayımlama ayarları dosyalarını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="33711-111">However, not all services support publish settings files.</span></span>
<span data-ttu-id="33711-112">Örneğin, **AzureResourceManager** modülü yayımlama ayarları dosyalarını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="33711-112">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="33711-113">**Güvenlik notu:** Yayımlama ayarları dosyaları kodlanmış ancak şifrelenmemiş bir yönetim sertifikası içerir.</span><span class="sxs-lookup"><span data-stu-id="33711-113">**Security Note:** Publish settings files contain a management certificate that is encoded, but not encrypted.</span></span>
<span data-ttu-id="33711-114">Kötü niyetli kullanıcılar yayımlama ayarları dosyanıza erişlerse, Azure hizmetlerini düzenleyebilir, oluşturabilir ve silebilir.</span><span class="sxs-lookup"><span data-stu-id="33711-114">If  malicious users access your publish settings file,  they might be able to edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="33711-115">En iyi güvenlik uygulaması olarak, dosyayı Indirmeler veya belgeler klasörünüzdeki bir konuma kaydedin ve sonra da ayarları içeri aktarmak için **import-azudandanayardandosya** cmdlet 'ini kullandıktan sonra silin.</span><span class="sxs-lookup"><span data-stu-id="33711-115">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

## <span data-ttu-id="33711-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33711-116">EXAMPLES</span></span>

### <span data-ttu-id="33711-117">Örnek 1: dosya Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="33711-117">Example 1: Import a file</span></span>
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

<span data-ttu-id="33711-118">Bu komut, "C:\Temp\MyAccount.publishsettings" dosyasını içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="33711-118">This command imports the "C:\Temp\MyAccount.publishsettings" file.</span></span>

## <span data-ttu-id="33711-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33711-119">PARAMETERS</span></span>

### <span data-ttu-id="33711-120">-Ortam</span><span class="sxs-lookup"><span data-stu-id="33711-120">-Environment</span></span>
<span data-ttu-id="33711-121">Bir Azure ortamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="33711-121">Specifies an Azure environment.</span></span>

<span data-ttu-id="33711-122">Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="33711-122">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="33711-123">Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="33711-123">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="33711-124">Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="33711-124">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33711-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="33711-125">-Profile</span></span>
<span data-ttu-id="33711-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="33711-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="33711-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="33711-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="33711-128">-PublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="33711-128">-PublishSettingsFile</span></span>
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

### <span data-ttu-id="33711-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33711-129">CommonParameters</span></span>
<span data-ttu-id="33711-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33711-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33711-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33711-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33711-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33711-132">INPUTS</span></span>

### <span data-ttu-id="33711-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="33711-133">None</span></span>
<span data-ttu-id="33711-134">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="33711-134">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="33711-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33711-135">OUTPUTS</span></span>

### <span data-ttu-id="33711-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="33711-136">None</span></span>
<span data-ttu-id="33711-137">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="33711-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="33711-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33711-138">NOTES</span></span>
* <span data-ttu-id="33711-139">"Yayımlama ayarları dosyası". publishsettings dosya adı uzantısına sahip bir XML dosyasıdır.</span><span class="sxs-lookup"><span data-stu-id="33711-139">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span> <span data-ttu-id="33711-140">Dosya, Azure abonelikleriniz için yönetim kimlik bilgilerini sağlayan kodlanmış bir sertifika içeriyor.</span><span class="sxs-lookup"><span data-stu-id="33711-140">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span> <span data-ttu-id="33711-141">Bu dosyayı içeri aktardıktan sonra güvenlik risklerini engellemek için dosyayı silin.</span><span class="sxs-lookup"><span data-stu-id="33711-141">After you import this file, delete it to avoid security risks.</span></span>
* <span data-ttu-id="33711-142">"Abonelik verileri dosyası", bilgisayarınıza güvenle kaydedibir XML dosyasıdır.</span><span class="sxs-lookup"><span data-stu-id="33711-142">A "subscription data file" is an XML file that can be saved on your computer safely.</span></span> <span data-ttu-id="33711-143">Varsayılan olarak, gezici kullanıcı profilinize ($home/AppData/Roaming) kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="33711-143">By default, it's saved in your roaming user profile ($home/AppData/Roaming).</span></span>

## <span data-ttu-id="33711-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33711-144">RELATED LINKS</span></span>

[<span data-ttu-id="33711-145">Azure PowerShell 'i yükleme ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="33711-145">How to Install and Configure Azure PowerShell</span></span>](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[<span data-ttu-id="33711-146">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="33711-146">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="33711-147">Get-Azuikinci dosyayı</span><span class="sxs-lookup"><span data-stu-id="33711-147">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)


