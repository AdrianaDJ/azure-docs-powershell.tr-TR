---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320953"
---
# <span data-ttu-id="f795b-101">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="f795b-101">New-AzDataFactoryEncryptValue</span></span>

## <span data-ttu-id="f795b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f795b-102">SYNOPSIS</span></span>
<span data-ttu-id="f795b-103">Hassas verileri şifreler.</span><span class="sxs-lookup"><span data-stu-id="f795b-103">Encrypts sensitive data.</span></span>

## <span data-ttu-id="f795b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f795b-104">SYNTAX</span></span>

### <span data-ttu-id="f795b-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f795b-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f795b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f795b-106">ByFactoryObject</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f795b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f795b-107">DESCRIPTION</span></span>
<span data-ttu-id="f795b-108">**Yeni-Azverifactoryencryptvalue** cmdlet 'i parola veya Microsoft SQL Server bağlantı dizesi gibi hassas verileri şifreler ve şifrelenmiş bir değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="f795b-108">The **New-AzDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="f795b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f795b-109">EXAMPLES</span></span>

### <span data-ttu-id="f795b-110">Örnek 1: ODBC dışı bağlantı dizesini şifreleme</span><span class="sxs-lookup"><span data-stu-id="f795b-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="f795b-111">İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak belirtilen bağlantı dizesini bir **SecureString** nesnesine dönüştürebilir ve bu nesneyi $Value değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f795b-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="f795b-112">Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="f795b-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="f795b-113">İzin verilen değerler: SQL Server veya Oracle bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="f795b-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="f795b-114">İkinci komut, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Value depolanan nesne için şifreli bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f795b-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="f795b-115">Örnek 2: Windows kimlik doğrulaması kullanan ODBC olmayan bir bağlantı dizesini şifreleyin.</span><span class="sxs-lookup"><span data-stu-id="f795b-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="f795b-116">İlk komut, **ConvertTo-SecureString** kullanarak belirtilen bağlantı dizesini güvenli bir dize nesnesine dönüştürebilir ve bu nesneyi $Value değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f795b-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="f795b-117">İkinci komut, Windows kimlik doğrulamasını (Kullanıcı adı ve parola) biriktirmek için Get-Credential cmdlet 'ini kullanır ve bu **PSCredential** nesnesini $Credential değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="f795b-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="f795b-118">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="f795b-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="f795b-119">Üçüncü komut, $Value depolanan nesne için, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Credential şifreli bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f795b-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="f795b-120">Örnek 3: dosya sistemi bağlantılı hizmeti için sunucu adını ve kimlik bilgilerini şifrele</span><span class="sxs-lookup"><span data-stu-id="f795b-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="f795b-121">İlk komut, **ConvertTo-SecureString** kullanarak belirtilen dizeyi güvenli bir dizeye dönüştürebilir ve bu nesneyi $Value değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f795b-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="f795b-122">İkinci komut, Windows kimlik doğrulamasını (Kullanıcı adı ve parola) biriktirmek için **Get-Credential** kullanır ve sonra bu **PSCredential** nesnesini $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f795b-122">The second command uses **Get-Credential** to collect the Windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="f795b-123">Üçüncü komut, $Value depolanan nesne için, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Credential şifreli bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f795b-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="f795b-124">Örnek 4: ".</span><span class="sxs-lookup"><span data-stu-id="f795b-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="f795b-125">**ConvertTo-SecureString** komutu belirtilen dizeyi güvenli dizeye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="f795b-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="f795b-126">**New-Object** komutu, güvenli Kullanıcı adı ve parola dizelerini kullanarak bir PSCredential nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f795b-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="f795b-127">Bunun yerine, **Get-Credential** komutunu kullanarak Windows kimlik doğrulamasını (Kullanıcı adı ve parola) toplayabilirsiniz ve ardından önceki örneklerde gösterildiği gibi $Credential değişkeninde döndürülen **PSCredential** nesnesini depolayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f795b-127">Instead, you could use the **Get-Credential** command to collect Windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="f795b-128">**Yeni-Azverifactoryencryptvalue** komutu, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $Credential depolanan nesne için şifreli bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f795b-128">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="f795b-129">Örnek 5: ODBC bağlantılı hizmeti için kimlik bilgilerini şifreleme</span><span class="sxs-lookup"><span data-stu-id="f795b-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="f795b-130">**ConvertTo-SecureString** komutu belirtilen dizeyi güvenli dizeye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="f795b-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="f795b-131">**Yeni-Azverifactoryencryptvalue** komutu, belirtilen veri fabrikası, ağ geçidi, kaynak grubu ve bağlantılı hizmet türü için $value depolanan nesne için şifreli bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f795b-131">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="f795b-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f795b-132">PARAMETERS</span></span>

### <span data-ttu-id="f795b-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f795b-133">-AuthenticationType</span></span>
<span data-ttu-id="f795b-134">Veri kaynağına bağlanmak için kullanılacak kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f795b-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="f795b-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f795b-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f795b-136">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="f795b-136">Windows</span></span>
- <span data-ttu-id="f795b-137">Ana</span><span class="sxs-lookup"><span data-stu-id="f795b-137">Basic</span></span>
- <span data-ttu-id="f795b-138">Belirtmeden.</span><span class="sxs-lookup"><span data-stu-id="f795b-138">Anonymous.</span></span>

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

### <span data-ttu-id="f795b-139">-Credential</span><span class="sxs-lookup"><span data-stu-id="f795b-139">-Credential</span></span>
<span data-ttu-id="f795b-140">Kullanılacak Windows kimlik doğrulama kimlik bilgilerini (Kullanıcı adı ve parola) belirtir.</span><span class="sxs-lookup"><span data-stu-id="f795b-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="f795b-141">Bu cmdlet burada belirttiğiniz kimlik bilgileri şifreler.</span><span class="sxs-lookup"><span data-stu-id="f795b-141">This cmdlet encrypts the credential data you specify here.</span></span>

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

### <span data-ttu-id="f795b-142">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="f795b-142">-Database</span></span>
<span data-ttu-id="f795b-143">Bağlı hizmetin veritabanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f795b-143">Specifies the database name of the linked service.</span></span>

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

### <span data-ttu-id="f795b-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f795b-144">-DataFactory</span></span>
<span data-ttu-id="f795b-145">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f795b-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f795b-146">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için verileri şifreler.</span><span class="sxs-lookup"><span data-stu-id="f795b-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f795b-147">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f795b-147">-DataFactoryName</span></span>
<span data-ttu-id="f795b-148">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f795b-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f795b-149">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için verileri şifreler.</span><span class="sxs-lookup"><span data-stu-id="f795b-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f795b-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f795b-150">-DefaultProfile</span></span>
<span data-ttu-id="f795b-151">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f795b-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f795b-152">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="f795b-152">-GatewayName</span></span>
<span data-ttu-id="f795b-153">Ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f795b-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="f795b-154">Bu cmdlet, bu parametrenin belirttiği ağ geçidi verilerini şifreler.</span><span class="sxs-lookup"><span data-stu-id="f795b-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f795b-155">-Credentialvalue</span><span class="sxs-lookup"><span data-stu-id="f795b-155">-NonCredentialValue</span></span>
<span data-ttu-id="f795b-156">Açık veritabanı bağlantısı (ODBC) bağlantı dizesinin kimlik bilgileri olmayan kısmını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f795b-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="f795b-157">Bu parametre yalnızca ODBC bağlantılı hizmeti için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="f795b-157">This parameter is applicable only for the ODBC linked service.</span></span>

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

### <span data-ttu-id="f795b-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f795b-158">-ResourceGroupName</span></span>
<span data-ttu-id="f795b-159">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f795b-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f795b-160">Bu cmdlet, bu parametrenin belirttiği grubun verilerini şifreler.</span><span class="sxs-lookup"><span data-stu-id="f795b-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f795b-161">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="f795b-161">-Server</span></span>
<span data-ttu-id="f795b-162">Bağlı hizmetin sunucu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f795b-162">Specifies the server name of the linked service.</span></span>

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

### <span data-ttu-id="f795b-163">-Tür</span><span class="sxs-lookup"><span data-stu-id="f795b-163">-Type</span></span>
<span data-ttu-id="f795b-164">Bağlı hizmet türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f795b-164">Specifies the linked service type.</span></span>
<span data-ttu-id="f795b-165">Bu cmdlet, bu parametrenin belirttiği bağlantılı hizmet türü için verileri şifreler.</span><span class="sxs-lookup"><span data-stu-id="f795b-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="f795b-166">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f795b-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f795b-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="f795b-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="f795b-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="f795b-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="f795b-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="f795b-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="f795b-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="f795b-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="f795b-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="f795b-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="f795b-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="f795b-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="f795b-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="f795b-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="f795b-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f795b-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="f795b-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="f795b-175">OnPremisesSybaseLinkedService</span></span>

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

### <span data-ttu-id="f795b-176">-Değer</span><span class="sxs-lookup"><span data-stu-id="f795b-176">-Value</span></span>
<span data-ttu-id="f795b-177">Şifrelenecek değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="f795b-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="f795b-178">Şirket içi bir SQL Server bağlantılı hizmeti ve şirket içi Oracle bağlantılı hizmeti için bir bağlantı dizesi kullanın.</span><span class="sxs-lookup"><span data-stu-id="f795b-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="f795b-179">Şirket içi ODBC bağlantılı hizmeti için, bağlantı dizesinin kimlik bilgileri bölümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="f795b-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="f795b-180">Şirket içi dosya sistemi bağlantılı hizmetinde, dosya sistemi ağ geçidi bilgisayarında yerelyse, yerel veya localhost kullanın ve dosya sistemi ağ geçidi bilgisayarından farklı bir \\ \\ sunucucudır, ServerName kullanın.</span><span class="sxs-lookup"><span data-stu-id="f795b-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

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

### <span data-ttu-id="f795b-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f795b-181">CommonParameters</span></span>
<span data-ttu-id="f795b-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f795b-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f795b-183">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f795b-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f795b-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f795b-184">INPUTS</span></span>

### <span data-ttu-id="f795b-185">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="f795b-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f795b-186">System. String</span><span class="sxs-lookup"><span data-stu-id="f795b-186">System.String</span></span>

## <span data-ttu-id="f795b-187">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f795b-187">OUTPUTS</span></span>

### <span data-ttu-id="f795b-188">System. String</span><span class="sxs-lookup"><span data-stu-id="f795b-188">System.String</span></span>

## <span data-ttu-id="f795b-189">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f795b-189">NOTES</span></span>
* <span data-ttu-id="f795b-190">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="f795b-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f795b-191">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f795b-191">RELATED LINKS</span></span>

[<span data-ttu-id="f795b-192">Yeni-Azveri Factoryencryptvalue</span><span class="sxs-lookup"><span data-stu-id="f795b-192">New-AzDataFactoryEncryptValue</span></span>](./New-AzDataFactoryEncryptValue.md)


