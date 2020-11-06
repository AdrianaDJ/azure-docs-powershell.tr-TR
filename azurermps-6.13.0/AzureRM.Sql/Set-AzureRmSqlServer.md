---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: e385d51a1fba06857b922ab9aabbd100e61b036e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593176"
---
# <span data-ttu-id="cd15b-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="cd15b-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="cd15b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd15b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd15b-103">SQL veritabanı sunucusunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd15b-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd15b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd15b-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd15b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd15b-105">DESCRIPTION</span></span>
<span data-ttu-id="cd15b-106">**Set-AzureRmSqlServer** cmdlet 'i, BIR Azure SQL veritabanı sunucusunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd15b-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="cd15b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd15b-107">EXAMPLES</span></span>

### <span data-ttu-id="cd15b-108">Örnek 1: yönetici parolasını sıfırlama</span><span class="sxs-lookup"><span data-stu-id="cd15b-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="cd15b-109">Bu komut, server01 adındaki AzureSQL sunucusundaki yönetici parolasını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="cd15b-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="cd15b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd15b-110">PARAMETERS</span></span>

### <span data-ttu-id="cd15b-111">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="cd15b-111">-AssignIdentity</span></span>
<span data-ttu-id="cd15b-112">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu sunucu için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="cd15b-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="cd15b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd15b-113">-DefaultProfile</span></span>
<span data-ttu-id="cd15b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cd15b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd15b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd15b-115">-Force</span></span>
<span data-ttu-id="cd15b-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="cd15b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd15b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd15b-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd15b-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd15b-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd15b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cd15b-119">-ServerName</span></span>
<span data-ttu-id="cd15b-120">Bu cmdlet 'in değiştirdiği sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd15b-120">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd15b-121">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="cd15b-121">-ServerVersion</span></span>
<span data-ttu-id="cd15b-122">Bu cmdlet 'in sunucuyu değiştirdiği sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd15b-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="cd15b-123">Bu parametre için kabul edilebilir değerler: 2,0 ve 12,0.</span><span class="sxs-lookup"><span data-stu-id="cd15b-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15b-124">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="cd15b-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="cd15b-125">Veritabanı sunucusu yöneticisi için **SecureString** olarak yeni bir parola belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd15b-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="cd15b-126">**SecureString** edinmek için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cd15b-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="cd15b-127">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="cd15b-127">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15b-128">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="cd15b-128">-Tags</span></span>
<span data-ttu-id="cd15b-129">Bu cmdlet 'in sunucuyla ilişki kurduğu etiketlerin sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd15b-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="cd15b-130">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="cd15b-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="cd15b-131">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="cd15b-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15b-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd15b-132">-Confirm</span></span>
<span data-ttu-id="cd15b-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd15b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd15b-134">-WhatIf</span></span>
<span data-ttu-id="cd15b-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd15b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd15b-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd15b-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd15b-137">CommonParameters</span></span>
<span data-ttu-id="cd15b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd15b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd15b-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd15b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd15b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd15b-140">INPUTS</span></span>

### <span data-ttu-id="cd15b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cd15b-141">System.String</span></span>

## <span data-ttu-id="cd15b-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd15b-142">OUTPUTS</span></span>

### <span data-ttu-id="cd15b-143">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="cd15b-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="cd15b-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd15b-144">NOTES</span></span>

## <span data-ttu-id="cd15b-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd15b-145">RELATED LINKS</span></span>

[<span data-ttu-id="cd15b-146">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="cd15b-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
