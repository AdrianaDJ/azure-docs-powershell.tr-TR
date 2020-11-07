---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
ms.openlocfilehash: 54a759370f39dcd3844d42d858d23f6c178a4d08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762706"
---
# <span data-ttu-id="180c7-101">New-AzureRmDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="180c7-101">New-AzureRmDataFactoryEncryptValue</span></span>

## <span data-ttu-id="180c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="180c7-102">SYNOPSIS</span></span>
<span data-ttu-id="180c7-103">Hassas verileri şifreler.</span><span class="sxs-lookup"><span data-stu-id="180c7-103">Encrypts sensitive data.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="180c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="180c7-104">SYNTAX</span></span>

### <span data-ttu-id="180c7-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="180c7-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="180c7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="180c7-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="180c7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="180c7-107">DESCRIPTION</span></span>
<span data-ttu-id="180c7-108">**Yeni-AzureRmDataFactoryEncryptValue** cmdlet 'i parola veya Microsoft SQL Server bağlantı dizesi gibi hassas verileri şifreler ve şifrelenmiş bir değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="180c7-108">The **New-AzureRmDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="180c7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="180c7-109">EXAMPLES</span></span>

### <span data-ttu-id="180c7-110">Örnek 1: ODBC dışı bağlantı dizesini şifreleme</span><span class="sxs-lookup"><span data-stu-id="180c7-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzureRmDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="180c7-111">İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak belirtilen bağlantı dizesini bir **SecureString** nesnesine dönüştürebilir ve bu nesneyi $Value değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="180c7-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="180c7-112">Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="180c7-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="180c7-113">İzin verilen değerler: SQL Server veya Oracle bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="180c7-113">Allowed values: SQL Server or Oracle connection string.</span></span>

<span data-ttu-id="180c7-114">İkinci komut, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Value depolanan nesne için şifreli bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="180c7-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="180c7-115">Örnek 2: Windows kimlik doğrulaması kullanan ODBC olmayan bir bağlantı dizesini şifreleyin.</span><span class="sxs-lookup"><span data-stu-id="180c7-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="180c7-116">İlk komut, **ConvertTo-SecureString** kullanarak belirtilen bağlantı dizesini güvenli bir dize nesnesine dönüştürebilir ve bu nesneyi $Value değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="180c7-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>

<span data-ttu-id="180c7-117">İkinci komut, Windows kimlik doğrulamasını (Kullanıcı adı ve parola) biriktirmek için Get-Credential cmdlet 'ini kullanır ve bu **PSCredential** nesnesini $Credential değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="180c7-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="180c7-118">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="180c7-118">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="180c7-119">Üçüncü komut, $Value depolanan nesne için, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Credential şifreli bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="180c7-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="180c7-120">Örnek 3: dosya sistemi bağlantılı hizmeti için sunucu adını ve kimlik bilgilerini şifrele</span><span class="sxs-lookup"><span data-stu-id="180c7-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="180c7-121">İlk komut, **ConvertTo-SecureString** kullanarak belirtilen dizeyi güvenli bir dizeye dönüştürebilir ve bu nesneyi $Value değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="180c7-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>

<span data-ttu-id="180c7-122">İkinci komut, Windows kimlik doğrulamasını (Kullanıcı adı ve parola) biriktirmek için **Get-Credential** kullanır ve sonra bu **PSCredential** nesnesini $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="180c7-122">The second command uses **Get-Credential** to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>

<span data-ttu-id="180c7-123">Üçüncü komut, $Value depolanan nesne için, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Credential şifreli bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="180c7-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="180c7-124">Örnek 4: ".</span><span class="sxs-lookup"><span data-stu-id="180c7-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzureRmDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="180c7-125">**ConvertTo-SecureString** komutu belirtilen dizeyi güvenli dizeye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="180c7-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="180c7-126">**New-Object** komutu, güvenli Kullanıcı adı ve parola dizelerini kullanarak bir PSCredential nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="180c7-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="180c7-127">Bunun yerine, **Get-Credential** komutunu kullanarak Windows kimlik doğrulamasını (Kullanıcı adı ve parola) toplayabilirsiniz ve ardından önceki örneklerde gösterildiği gibi $Credential değişkeninde döndürülen **PSCredential** nesnesini depolayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="180c7-127">Instead, you could use the **Get-Credential** command to collect windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>

<span data-ttu-id="180c7-128">**Yeni-AzureRmDataFactoryEncryptValue** komutu, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Credential depolanan nesne için şifrelenmiş bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="180c7-128">The **New-AzureRmDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="180c7-129">Örnek 5: ODBC bağlantılı hizmeti için kimlik bilgilerini şifreleme</span><span class="sxs-lookup"><span data-stu-id="180c7-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzureRmDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="180c7-130">**ConvertTo-SecureString** komutu belirtilen dizeyi güvenli dizeye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="180c7-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>

<span data-ttu-id="180c7-131">**Yeni-AzureRmDataFactoryEncryptValue** komutu, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $value depolanan nesne için şifrelenmiş bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="180c7-131">The **New-AzureRmDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="180c7-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="180c7-132">PARAMETERS</span></span>

### <span data-ttu-id="180c7-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="180c7-133">-AuthenticationType</span></span>
<span data-ttu-id="180c7-134">Veri kaynağına bağlanmak için kullanılacak kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="180c7-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="180c7-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="180c7-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="180c7-136">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="180c7-136">Windows</span></span>
- <span data-ttu-id="180c7-137">Ana</span><span class="sxs-lookup"><span data-stu-id="180c7-137">Basic</span></span>
- <span data-ttu-id="180c7-138">Belirtmeden.</span><span class="sxs-lookup"><span data-stu-id="180c7-138">Anonymous.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-139">-Credential</span><span class="sxs-lookup"><span data-stu-id="180c7-139">-Credential</span></span>
<span data-ttu-id="180c7-140">Kullanılacak Windows kimlik doğrulama kimlik bilgilerini (Kullanıcı adı ve parola) belirtir.</span><span class="sxs-lookup"><span data-stu-id="180c7-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="180c7-141">Bu cmdlet burada belirttiğiniz kimlik bilgileri şifreler.</span><span class="sxs-lookup"><span data-stu-id="180c7-141">This cmdlet encrypts the credential data you specify here.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-142">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="180c7-142">-Database</span></span>
<span data-ttu-id="180c7-143">Bağlı hizmetin veritabanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="180c7-143">Specifies the database name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="180c7-144">-DataFactory</span></span>
<span data-ttu-id="180c7-145">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="180c7-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="180c7-146">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için verileri şifreler.</span><span class="sxs-lookup"><span data-stu-id="180c7-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-147">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="180c7-147">-DataFactoryName</span></span>
<span data-ttu-id="180c7-148">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="180c7-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="180c7-149">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için verileri şifreler.</span><span class="sxs-lookup"><span data-stu-id="180c7-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-150">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="180c7-150">-GatewayName</span></span>
<span data-ttu-id="180c7-151">Ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="180c7-151">Specifies the name of the gateway.</span></span>
<span data-ttu-id="180c7-152">Bu cmdlet, bu parametrenin belirttiği ağ geçidi verilerini şifreler.</span><span class="sxs-lookup"><span data-stu-id="180c7-152">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-153">-Credentialvalue</span><span class="sxs-lookup"><span data-stu-id="180c7-153">-NonCredentialValue</span></span>
<span data-ttu-id="180c7-154">Açık veritabanı bağlantısı (ODBC) bağlantı dizesinin kimlik bilgileri olmayan kısmını belirtir.</span><span class="sxs-lookup"><span data-stu-id="180c7-154">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="180c7-155">Bu parametre yalnızca ODBC bağlantılı hizmeti için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="180c7-155">This parameter is applicable only for the ODBC linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="180c7-156">-ResourceGroupName</span></span>
<span data-ttu-id="180c7-157">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="180c7-157">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="180c7-158">Bu cmdlet, bu parametrenin belirttiği grubun verilerini şifreler.</span><span class="sxs-lookup"><span data-stu-id="180c7-158">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-159">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="180c7-159">-Server</span></span>
<span data-ttu-id="180c7-160">Bağlı hizmetin sunucu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="180c7-160">Specifies the server name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-161">-Tür</span><span class="sxs-lookup"><span data-stu-id="180c7-161">-Type</span></span>
<span data-ttu-id="180c7-162">Bağlı hizmet türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="180c7-162">Specifies the linked service type.</span></span>
<span data-ttu-id="180c7-163">Bu cmdlet, bu parametrenin belirttiği bağlantılı hizmet türü için verileri şifreler.</span><span class="sxs-lookup"><span data-stu-id="180c7-163">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="180c7-164">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="180c7-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="180c7-165">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="180c7-165">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="180c7-166">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="180c7-166">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="180c7-167">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="180c7-167">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="180c7-168">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="180c7-168">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="180c7-169">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="180c7-169">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="180c7-170">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="180c7-170">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="180c7-171">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="180c7-171">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="180c7-172">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="180c7-172">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="180c7-173">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="180c7-173">OnPremisesSybaseLinkedService</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-174">-Değer</span><span class="sxs-lookup"><span data-stu-id="180c7-174">-Value</span></span>
<span data-ttu-id="180c7-175">Şifrelenecek değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="180c7-175">Specifies the value to encrypt.</span></span>
<span data-ttu-id="180c7-176">Şirket içi bir SQL Server bağlantılı hizmeti ve şirket içi Oracle bağlantılı hizmeti için bir bağlantı dizesi kullanın.</span><span class="sxs-lookup"><span data-stu-id="180c7-176">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="180c7-177">Şirket içi ODBC bağlantılı hizmeti için, bağlantı dizesinin kimlik bilgileri bölümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="180c7-177">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="180c7-178">Şirket içi dosya sistemi bağlantılı hizmetinde, dosya sistemi ağ geçidi bilgisayarında yerelyse, yerel veya localhost kullanın ve dosya sistemi ağ geçidi bilgisayarından farklı bir \\ \\ sunucucudır, ServerName kullanın.</span><span class="sxs-lookup"><span data-stu-id="180c7-178">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-179">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="180c7-179">-DefaultProfile</span></span>
<span data-ttu-id="180c7-180">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="180c7-180">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180c7-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="180c7-181">CommonParameters</span></span>
<span data-ttu-id="180c7-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="180c7-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="180c7-183">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="180c7-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="180c7-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="180c7-184">INPUTS</span></span>

## <span data-ttu-id="180c7-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="180c7-185">OUTPUTS</span></span>

### <span data-ttu-id="180c7-186">System. String</span><span class="sxs-lookup"><span data-stu-id="180c7-186">System.String</span></span>

## <span data-ttu-id="180c7-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="180c7-187">NOTES</span></span>
* <span data-ttu-id="180c7-188">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="180c7-188">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="180c7-189">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="180c7-189">RELATED LINKS</span></span>

[<span data-ttu-id="180c7-190">Yeni-AzureRmDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="180c7-190">New-AzureRmDataFactoryEncryptValue</span></span>](./New-AzureRmDataFactoryEncryptValue.md)


