---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105970"
---
# <span data-ttu-id="9c5db-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="9c5db-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="9c5db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c5db-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5db-103">Sunucu bağlantı bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9c5db-103">Creates a server connection context.</span></span>

## <span data-ttu-id="9c5db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c5db-104">SYNTAX</span></span>

### <span data-ttu-id="9c5db-105">ByServerNameWithSqlAuth (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9c5db-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c5db-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="9c5db-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9c5db-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="9c5db-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9c5db-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="9c5db-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9c5db-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="9c5db-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c5db-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c5db-110">DESCRIPTION</span></span>
<span data-ttu-id="9c5db-111">**New-Azuressqldatabaseservercontext** cmdlet 'ı Azure SQL veritabanı sunucusu bağlantı bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9c5db-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="9c5db-112">Belirtilen kimlik bilgilerini kullanarak SQL veritabanı sunucusuna bağlantı bağlamı oluşturmak için SQL Server kimlik doğrulamasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="9c5db-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="9c5db-113">SQL veritabanı sunucusunu ad veya URL ile belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c5db-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="9c5db-114">Kimlik bilgilerini almak için, Kullanıcı adını ve parolayı belirtmenizi isteyen Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9c5db-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="9c5db-115">Belirtilen Azure aboneliği verilerini kullanarak belirtilen SQL veritabanı sunucusuna bir bağlantı bağlamı oluşturmak için, sertifika tabanlı kimlik doğrulama ile **Yeni-Azuressqldatabaseservercontext** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9c5db-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="9c5db-116">SQL veritabanı sunucusunu ada göre veya tam adı ile belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c5db-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="9c5db-117">Abonelik verilerini parametre olarak belirtebilirsiniz veya geçerli Azure aboneliğinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="9c5db-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="9c5db-118"> https://msdn.microsoft.com/library/windowsazure/jj152833.aspxGeçerli Azure aboneliğini seçmek Için Select-azuyeniden</span><span class="sxs-lookup"><span data-stu-id="9c5db-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="9c5db-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c5db-119">EXAMPLES</span></span>

### <span data-ttu-id="9c5db-120">Örnek 1: SQL Server kimlik doğrulamasını kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="9c5db-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="9c5db-121">Bu örnekte SQL Server kimlik doğrulaması kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9c5db-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="9c5db-122">İlk komut sizden Sunucu Yöneticisi kimlik bilgilerini sorar ve $Credential değişkeninde kimlik bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="9c5db-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="9c5db-123">İkinci komut, $Credential kullanarak lpqd0zbr8y adlı SQL veritabanı sunucusuna bağlanır.</span><span class="sxs-lookup"><span data-stu-id="9c5db-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="9c5db-124">Son komut, $Context içeriğin parçası olan sunucuda Database17 adlı bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9c5db-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="9c5db-125">Örnek 2: sertifika tabanlı kimlik doğrulaması kullanarak bağlam oluşturma</span><span class="sxs-lookup"><span data-stu-id="9c5db-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="9c5db-126">Bu örnekte sertifika tabanlı kimlik doğrulama kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9c5db-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="9c5db-127">İlk iki komut $SubscriptionId ve $Thumbprint değişkenlerine değerler atar.</span><span class="sxs-lookup"><span data-stu-id="9c5db-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="9c5db-128">Üçüncü komut $Thumbprint 'da parmak iziyle tanımlanan sertifikayı alır ve $Certificate depolar.</span><span class="sxs-lookup"><span data-stu-id="9c5db-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="9c5db-129">Dördüncü komut, aboneliği Subscription07 olarak ayarlar ve beşinci komut bu aboneliği seçer.</span><span class="sxs-lookup"><span data-stu-id="9c5db-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="9c5db-130">Son komutu, lpqd0zbr8y adlı sunucudaki geçerli abonelikte bir bağlam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9c5db-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="9c5db-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c5db-131">PARAMETERS</span></span>

### <span data-ttu-id="9c5db-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="9c5db-132">-Credential</span></span>
<span data-ttu-id="9c5db-133">Sunucuya erişmeniz için SQL Server kimlik doğrulamasını sağlayan bir kimlik bilgisi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c5db-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5db-134">-Tamyqualifiedservername</span><span class="sxs-lookup"><span data-stu-id="9c5db-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="9c5db-135">Azure SQL veritabanı sunucusu için tam etki alanı adı (FQDN) adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c5db-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="9c5db-136">Örneğin, Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="9c5db-136">For example, Server02.database.windows.net.</span></span>

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5db-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="9c5db-137">-ManageUrl</span></span>
<span data-ttu-id="9c5db-138">Bu cmdlet 'in sunucunun Azure SQL DatabaseManagement portalına kullandığı URL 'YI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c5db-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5db-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="9c5db-139">-Profile</span></span>
<span data-ttu-id="9c5db-140">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c5db-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c5db-141">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9c5db-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9c5db-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9c5db-142">-ServerName</span></span>
<span data-ttu-id="9c5db-143">Veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c5db-143">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c5db-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9c5db-144">-SubscriptionName</span></span>
<span data-ttu-id="9c5db-145">Bu cmdlet 'in bağlantı bağlamını oluşturmak için kullandığı Azure aboneliğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c5db-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="9c5db-146">Bu parametre için bir değer belirtmezseniz, cmdlet geçerli aboneliği kullanır.</span><span class="sxs-lookup"><span data-stu-id="9c5db-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="9c5db-147">Geçerli aboneliği değiştirmek için Select-AzureSubscription cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="9c5db-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c5db-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="9c5db-148">-UseSubscription</span></span>
<span data-ttu-id="9c5db-149">Bu cmdlet 'in bağlantı bağlamını oluşturmak için Azure aboneliğini kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c5db-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5db-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5db-150">CommonParameters</span></span>
<span data-ttu-id="9c5db-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c5db-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5db-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5db-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5db-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c5db-153">INPUTS</span></span>

## <span data-ttu-id="9c5db-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c5db-154">OUTPUTS</span></span>

### <span data-ttu-id="9c5db-155">Microsoft. Windowsazde. Commands. SqlDatabase. Services. Server. IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="9c5db-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="9c5db-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c5db-156">NOTES</span></span>
* <span data-ttu-id="9c5db-157">Etki alanı belirtmeden kimlik doğrulatın ve Windows PowerShell 2,0 kullanıyorsanız, Get-Credential cmdlet 'i bir ters eğik çizgi () döndürür; \\ Örneğin, Kullanıcı1.</span><span class="sxs-lookup"><span data-stu-id="9c5db-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="9c5db-158">Windows PowerShell 3,0 ters eğik çizgiyi eklemez.</span><span class="sxs-lookup"><span data-stu-id="9c5db-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="9c5db-159">Bu ters eğik çizgi, **New-Azuressqldatabaseservercontext** cmdlet 'inin *Credential* parametresi tarafından tanınmaz.</span><span class="sxs-lookup"><span data-stu-id="9c5db-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="9c5db-160">Kaldırmak için, aşağıdakine benzer komutları kullanın:</span><span class="sxs-lookup"><span data-stu-id="9c5db-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="9c5db-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c5db-161">RELATED LINKS</span></span>

[<span data-ttu-id="9c5db-162">Azure SQL veritabanı cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="9c5db-162">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="9c5db-163">Get-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="9c5db-163">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="9c5db-164">Yeni-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="9c5db-164">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="9c5db-165">Remove-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="9c5db-165">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="9c5db-166">Set-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="9c5db-166">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


