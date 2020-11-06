---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 333de53ccd3632188100af7f3fcde10e140537c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591896"
---
# <span data-ttu-id="d2a1b-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="d2a1b-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="d2a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a1b-103">Verilen SQL Server örneğine bir saydam veri şifreleme sertifikası ekler</span><span class="sxs-lookup"><span data-stu-id="d2a1b-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2a1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2a1b-104">SYNTAX</span></span>

### <span data-ttu-id="d2a1b-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2a1b-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2a1b-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2a1b-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2a1b-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2a1b-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2a1b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2a1b-108">DESCRIPTION</span></span>
<span data-ttu-id="d2a1b-109">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate, verilen SQL Server örneğine bir saydam veri şifreleme sertifikası ekler</span><span class="sxs-lookup"><span data-stu-id="d2a1b-109">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="d2a1b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2a1b-110">EXAMPLES</span></span>

### <span data-ttu-id="d2a1b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d2a1b-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="d2a1b-112">Kaynak grubu adını ve SQL Server adını kullanarak bir SQL sunucusuna ton sertifikası ekleme</span><span class="sxs-lookup"><span data-stu-id="d2a1b-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="d2a1b-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d2a1b-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzureRmSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="d2a1b-114">Sunucu ResourceId kullanarak sunuculara TDE sertifikası ekleme</span><span class="sxs-lookup"><span data-stu-id="d2a1b-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="d2a1b-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d2a1b-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzureRmSqlServer | Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="d2a1b-116">Kaynak grubundaki tüm SQL sunucularına TDE sertifikası ekleme</span><span class="sxs-lookup"><span data-stu-id="d2a1b-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="d2a1b-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2a1b-117">PARAMETERS</span></span>

### <span data-ttu-id="d2a1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a1b-118">-DefaultProfile</span></span>
<span data-ttu-id="d2a1b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2a1b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2a1b-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d2a1b-120">-PassThru</span></span>
<span data-ttu-id="d2a1b-121">Başarılı bir yürütmede, eklenen sertifika nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="d2a1b-121">On Successful execution, returns certificate object that was added.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1b-122">-Parola</span><span class="sxs-lookup"><span data-stu-id="d2a1b-122">-Password</span></span>
<span data-ttu-id="d2a1b-123">Saydam veri şifreleme sertifikasının parolası</span><span class="sxs-lookup"><span data-stu-id="d2a1b-123">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1b-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="d2a1b-124">-PrivateBlob</span></span>
<span data-ttu-id="d2a1b-125">Saydam veri şifreleme sertifikası için özel blob</span><span class="sxs-lookup"><span data-stu-id="d2a1b-125">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a1b-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2a1b-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d2a1b-127">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1b-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d2a1b-128">-ServerName</span></span>
<span data-ttu-id="d2a1b-129">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="d2a1b-129">The Server Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1b-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="d2a1b-130">-SqlServer</span></span>
<span data-ttu-id="d2a1b-131">SQL Server giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="d2a1b-131">The sql server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1b-132">-Sqlserverresourceıd</span><span class="sxs-lookup"><span data-stu-id="d2a1b-132">-SqlServerResourceId</span></span>
<span data-ttu-id="d2a1b-133">SQL Server kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d2a1b-133">The sql server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1b-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2a1b-134">-Confirm</span></span>
<span data-ttu-id="d2a1b-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2a1b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2a1b-136">-WhatIf</span></span>
<span data-ttu-id="d2a1b-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2a1b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2a1b-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2a1b-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a1b-139">CommonParameters</span></span>
<span data-ttu-id="d2a1b-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2a1b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a1b-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a1b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a1b-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2a1b-142">INPUTS</span></span>

### <span data-ttu-id="d2a1b-143">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="d2a1b-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="d2a1b-144">Parametreler: SqlServer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d2a1b-144">Parameters: SqlServer (ByValue)</span></span>

### <span data-ttu-id="d2a1b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d2a1b-145">System.String</span></span>

## <span data-ttu-id="d2a1b-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2a1b-146">OUTPUTS</span></span>

### <span data-ttu-id="d2a1b-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2a1b-147">System.Boolean</span></span>

## <span data-ttu-id="d2a1b-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2a1b-148">NOTES</span></span>

## <span data-ttu-id="d2a1b-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2a1b-149">RELATED LINKS</span></span>
