---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: 6b9fa4c7fff426f9af19484c7576b9dee341a82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762830"
---
# <span data-ttu-id="78a97-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="78a97-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="78a97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a97-102">SYNOPSIS</span></span>
<span data-ttu-id="78a97-103">SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="78a97-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78a97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78a97-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78a97-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="78a97-105">DESCRIPTION</span></span>
<span data-ttu-id="78a97-106">**New-AzureRmSqlServer** cmdlet 'ı BIR Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="78a97-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="78a97-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78a97-107">EXAMPLES</span></span>

### <span data-ttu-id="78a97-108">Örnek 1: yeni Azure SQL veritabanı sunucusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="78a97-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="78a97-109">Bu komut 12 Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="78a97-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="78a97-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78a97-110">PARAMETERS</span></span>

### <span data-ttu-id="78a97-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="78a97-111">-AsJob</span></span>
<span data-ttu-id="78a97-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="78a97-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="78a97-113">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="78a97-113">-AssignIdentity</span></span>
<span data-ttu-id="78a97-114">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu sunucu için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="78a97-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="78a97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a97-115">-DefaultProfile</span></span>
<span data-ttu-id="78a97-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="78a97-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a97-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="78a97-117">-Location</span></span>
<span data-ttu-id="78a97-118">Bu cmdlet 'in sunucuyu oluşturduğu veri merkezinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a97-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a97-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a97-119">-ResourceGroupName</span></span>
<span data-ttu-id="78a97-120">Bu cmdlet 'in sunucuya atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a97-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78a97-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="78a97-121">-ServerName</span></span>
<span data-ttu-id="78a97-122">Yeni sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a97-122">Specifies the name of the new server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a97-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="78a97-123">-ServerVersion</span></span>
<span data-ttu-id="78a97-124">Yeni sunucunun sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a97-124">Specifies the version of the new server.</span></span> <span data-ttu-id="78a97-125">Bu parametre için kabul edilebilir değerler: 2,0 ve 12,0.</span><span class="sxs-lookup"><span data-stu-id="78a97-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="78a97-126">Sürüm 11 sunucusu oluşturmak için 2,0 veya sürüm 12 sunucusu oluşturmak için 12,0.</span><span class="sxs-lookup"><span data-stu-id="78a97-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="78a97-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="78a97-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="78a97-128">Yeni sunucunun SQL veritabanı sunucusu yöneticisi kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a97-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="78a97-129">**PSCredential** nesnesi almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="78a97-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="78a97-130">Daha fazla bilgi için yazın `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="78a97-130">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a97-131">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="78a97-131">-Tags</span></span>
<span data-ttu-id="78a97-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="78a97-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="78a97-133">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="78a97-133">For example:</span></span>

<span data-ttu-id="78a97-134">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="78a97-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a97-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="78a97-135">-Confirm</span></span>
<span data-ttu-id="78a97-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="78a97-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78a97-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78a97-137">-WhatIf</span></span>
<span data-ttu-id="78a97-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="78a97-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78a97-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="78a97-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78a97-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a97-140">CommonParameters</span></span>
<span data-ttu-id="78a97-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78a97-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a97-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a97-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a97-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78a97-143">INPUTS</span></span>

### <span data-ttu-id="78a97-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="78a97-144">None</span></span>
<span data-ttu-id="78a97-145">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="78a97-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78a97-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78a97-146">OUTPUTS</span></span>

### <span data-ttu-id="78a97-147">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="78a97-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="78a97-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78a97-148">NOTES</span></span>

## <span data-ttu-id="78a97-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78a97-149">RELATED LINKS</span></span>

[<span data-ttu-id="78a97-150">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="78a97-150">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="78a97-151">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="78a97-151">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="78a97-152">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="78a97-152">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="78a97-153">Yeni-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="78a97-153">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="78a97-154">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="78a97-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
