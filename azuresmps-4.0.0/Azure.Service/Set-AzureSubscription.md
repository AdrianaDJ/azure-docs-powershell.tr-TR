---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105950"
---
# <span data-ttu-id="6bd40-101">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="6bd40-101">Set-AzureSubscription</span></span>

## <span data-ttu-id="6bd40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bd40-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd40-103">Azure aboneliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6bd40-103">Changes an Azure subscription.</span></span>

## <span data-ttu-id="6bd40-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bd40-104">SYNTAX</span></span>

### <span data-ttu-id="6bd40-105">Updatesubscriptionbyıdparametersetname (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6bd40-105">UpdateSubscriptionByIdParameterSetName (Default)</span></span>
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6bd40-106">UpdateSubscriptionByNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6bd40-106">UpdateSubscriptionByNameParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6bd40-107">AddSubscriptionParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6bd40-107">AddSubscriptionParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bd40-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bd40-108">DESCRIPTION</span></span>
<span data-ttu-id="6bd40-109">**Set-azuyeniden gönderme Betikleşme** , bir Azure abonelik nesnesinin özelliklerini oluşturur ve değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6bd40-109">The **Set-AzureSubscription** cmdlet establishes and changes the properties of an Azure subscription object.</span></span>
<span data-ttu-id="6bd40-110">Varsayılan aboneliğiniz olmayan bir Azure aboneliğiyle çalışmak veya geçerli depolama hesabınızı değiştirmek için bu cmdlet 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6bd40-110">You can use this cmdlet to work in an Azure subscription that is not your default subscription or to change your current storage account.</span></span>
<span data-ttu-id="6bd40-111">Geçerli ve varsayılan abonelikler hakkında bilgi için, **Select-Azuyeniden komut Scription** cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="6bd40-111">For information about current and default subscriptions, see the **Select-AzureSubscription** cmdlet.</span></span>

<span data-ttu-id="6bd40-112">Bu cmdlet, gerçek Azure aboneliğinizi değil, bir Azure aboneliği nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="6bd40-112">This cmdlet operates on an Azure subscription object, not your actual Azure subscription.</span></span>
<span data-ttu-id="6bd40-113">Bir Azure aboneliği oluşturmak ve sağlamak için, [Azure portalını](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="6bd40-113">To create and provision an Azure subscription, visit the [Azure Portal](https://azure.microsoft.com/) (https://azure.microsoft.com/).</span></span>

<span data-ttu-id="6bd40-114">Bu cmdlet, Windows PowerShell 'e bir Azure hesabı eklemek için **Add-AzureAccount** veya **Import-Azuyeniden yükleyen SettingsFile** cmdlet 'ini kullandığınızda oluşturduğunuz abonelik verileri dosyasındaki verileri değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6bd40-114">This cmdlet changes the data in the subscription data file that you create when you use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** cmdlet to add an Azure account to Windows PowerShell.</span></span>

<span data-ttu-id="6bd40-115">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6bd40-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6bd40-116">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6bd40-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="6bd40-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bd40-117">EXAMPLES</span></span>

### <span data-ttu-id="6bd40-118">Örnek 1: varolan bir subscription1</span><span class="sxs-lookup"><span data-stu-id="6bd40-118">Example 1: Change an existing subscription1</span></span>
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

<span data-ttu-id="6bd40-119">Bu örnek, ContosoEngineering adlı aboneliğin sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6bd40-119">This example changes the certificate for the subscription named ContosoEngineering.</span></span>

### <span data-ttu-id="6bd40-120">Örnek 2: hizmet uç noktasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="6bd40-120">Example 2: Change the service endpoint</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

<span data-ttu-id="6bd40-121">Bu komut, ContosoEngineering aboneliği için özel bir hizmet uç noktası ekler veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6bd40-121">This command adds or changes a custom service endpoint for the ContosoEngineering subscription.</span></span>

### <span data-ttu-id="6bd40-122">Örnek 3: özellik değerlerini Temizleme</span><span class="sxs-lookup"><span data-stu-id="6bd40-122">Example 3: Clear property values</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

<span data-ttu-id="6bd40-123">Bu komut, sertifika ve ResourceManagerEndpoint özelliklerinin değerlerini null ($Null) olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6bd40-123">This command sets the values of the Certificate and ResourceManagerEndpoint properties to null ($Null).</span></span>
<span data-ttu-id="6bd40-124">Bu, diğer ayarları değiştirmeden bu özelliklerin değerlerini temizler.</span><span class="sxs-lookup"><span data-stu-id="6bd40-124">This clears the values of those properties without changing other settings.</span></span>

### <span data-ttu-id="6bd40-125">Örnek 4: alternatif bir abonelik veri dosyası kullanın</span><span class="sxs-lookup"><span data-stu-id="6bd40-125">Example 4: Use an alternate subscription data file</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

<span data-ttu-id="6bd40-126">Bu komut ContosoFinance aboneliğinin geçerli depolama hesabını ContosoStorage01 olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6bd40-126">This command changes the current storage account of the ContosoFinance subscription to ContosoStorage01.</span></span>
<span data-ttu-id="6bd40-127">Komut, C:\Azure\SubscriptionData.xml aboneliği veri dosyasındaki verileri değiştirmek için **subscriptionveri** dosyası parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6bd40-127">The command uses the **SubscriptionDataFile** parameter to change the data in the C:\Azure\SubscriptionData.xml subscription data file.</span></span>
<span data-ttu-id="6bd40-128">Varsayılan olarak **set-Azuyeniden gönderme betikte** , gezici kullanıcı profilinizde varsayılan abonelik verileri dosyası kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6bd40-128">By default, **Set-AzureSubscription** uses the default subscription data file in your roaming user profile.</span></span>

## <span data-ttu-id="6bd40-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bd40-129">PARAMETERS</span></span>

### <span data-ttu-id="6bd40-130">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="6bd40-130">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd40-131">-Context</span><span class="sxs-lookup"><span data-stu-id="6bd40-131">-Context</span></span>
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd40-132">-CurrentStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6bd40-132">-CurrentStorageAccountName</span></span>
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

### <span data-ttu-id="6bd40-133">-Ortam</span><span class="sxs-lookup"><span data-stu-id="6bd40-133">-Environment</span></span>
<span data-ttu-id="6bd40-134">Bir Azure ortamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd40-134">Specifies an Azure environment.</span></span>

<span data-ttu-id="6bd40-135">Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="6bd40-135">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="6bd40-136">Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6bd40-136">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="6bd40-137">Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6bd40-137">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="6bd40-138">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6bd40-138">-PassThru</span></span>
<span data-ttu-id="6bd40-139">Komut başarılı olduysa $True ve başarısız olursa $False döndürür.</span><span class="sxs-lookup"><span data-stu-id="6bd40-139">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="6bd40-140">Varsayılan olarak, bu cmdlet hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="6bd40-140">By default, this cmdlet does not return any output.</span></span>
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

### <span data-ttu-id="6bd40-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="6bd40-141">-Profile</span></span>
<span data-ttu-id="6bd40-142">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd40-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6bd40-143">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6bd40-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6bd40-144">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6bd40-144">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="6bd40-145">Hesap ile ilişkili kaynak gruplarıyla ilgili veriler de içinde olmak üzere, Azure Resource Manager verilerinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd40-145">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="6bd40-146">Azure Resource Manager hakkında daha fazla bilgi için [Azure Resource Manager cmdlet 'lerinin](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) ve [Kaynak Yöneticisi ile Windows PowerShell](https://go.microsoft.com/fwlink/?LinkID=394767)  'in ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="6bd40-146">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="6bd40-147">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6bd40-147">-ServiceEndpoint</span></span>
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

### <span data-ttu-id="6bd40-148">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6bd40-148">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd40-149">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6bd40-149">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd40-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd40-150">CommonParameters</span></span>
<span data-ttu-id="6bd40-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bd40-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd40-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bd40-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd40-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bd40-153">INPUTS</span></span>

### <span data-ttu-id="6bd40-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6bd40-154">None</span></span>
<span data-ttu-id="6bd40-155">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6bd40-155">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="6bd40-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bd40-156">OUTPUTS</span></span>

### <span data-ttu-id="6bd40-157">None veya System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6bd40-157">None or System.Boolean</span></span>
<span data-ttu-id="6bd40-158">*Passin* parametresini kullandığınızda, bu cmdlet bir Boole değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="6bd40-158">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="6bd40-159">Varsayılan olarak, bu cmdlet hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="6bd40-159">By default, this cmdlet does not return any output.</span></span>

## <span data-ttu-id="6bd40-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bd40-160">NOTES</span></span>

## <span data-ttu-id="6bd40-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bd40-161">RELATED LINKS</span></span>

[<span data-ttu-id="6bd40-162">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="6bd40-162">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="6bd40-163">Get-Azuyeniden gönderme</span><span class="sxs-lookup"><span data-stu-id="6bd40-163">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="6bd40-164">Import-Azuyeniden yayımlayan ayarları dosyası</span><span class="sxs-lookup"><span data-stu-id="6bd40-164">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="6bd40-165">Remove-Azuyeniden gönderiliyor</span><span class="sxs-lookup"><span data-stu-id="6bd40-165">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="6bd40-166">Select-Azuyeniden gönderme</span><span class="sxs-lookup"><span data-stu-id="6bd40-166">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)


