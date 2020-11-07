---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: fddefaf27d1e5b481bd90058739d472d7c793a88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938004"
---
# <span data-ttu-id="02391-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="02391-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="02391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02391-102">SYNOPSIS</span></span>
<span data-ttu-id="02391-103">SQL Server için Azure AD yöneticisi sağlar.</span><span class="sxs-lookup"><span data-stu-id="02391-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="02391-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02391-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [[-IsAzureADOnlyAuthentication] <Boolean>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02391-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="02391-105">DESCRIPTION</span></span>
<span data-ttu-id="02391-106">**Set-AzSqlServerActiveDirectoryAdministrator** cmdlet 'i, geçerli abonelikteki AzureSQL Server Için Azure Active Directory (Azure AD) Yöneticisi sağlar.</span><span class="sxs-lookup"><span data-stu-id="02391-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="02391-107">Aynı anda yalnızca bir yönetici temin edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02391-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="02391-108">Aşağıdaki Azure AD üyeleri SQL Server Yöneticisi olarak sağlanabilir:</span><span class="sxs-lookup"><span data-stu-id="02391-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="02391-109">Yerel Azure AD üyeleri</span><span class="sxs-lookup"><span data-stu-id="02391-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="02391-110">Şirket içindeki Federasyon üyeleri</span><span class="sxs-lookup"><span data-stu-id="02391-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="02391-111">Yerel veya Federasyon üyesi olan diğer Azure reklamlardan alınan Üyeler</span><span class="sxs-lookup"><span data-stu-id="02391-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="02391-112">Güvenlik grupları olarak oluşturulan Azure AD grupları, Outlook.com, Hotmail.com veya Live.com etki alanlarında olduğu gibi, yöneticiler tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="02391-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="02391-113">Gmail.com veya Yahoo.com etki alanlarında olduğu gibi diğer Konuk hesapları yöneticiler tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="02391-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="02391-114">Adanmış bir Azure AD grubunu yönetici olarak sağlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="02391-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="02391-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02391-115">EXAMPLES</span></span>

### <span data-ttu-id="02391-116">Örnek 1: sunucu için yönetici grubu hazırlama</span><span class="sxs-lookup"><span data-stu-id="02391-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="02391-117">Bu komut, server01 adlı sunucu için Vseçbas adlı bir Azure AD Yöneticisi grubu sağlar.</span><span class="sxs-lookup"><span data-stu-id="02391-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="02391-118">Bu sunucu, kaynak grubu ResourceGroup01 ile ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="02391-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="02391-119">Örnek 2: sunucu için Yönetici Kullanıcı sağlama</span><span class="sxs-lookup"><span data-stu-id="02391-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="02391-120">Bu komut, server01 adlı sunucunun yöneticisi olarak bir Azure AD kullanıcısı sağlar.</span><span class="sxs-lookup"><span data-stu-id="02391-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="02391-121">Örnek 3: KIMLIĞINI belirterek yönetici grubu hazırlama</span><span class="sxs-lookup"><span data-stu-id="02391-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="02391-122">Bu komut, server01 adlı sunucu için Vseçbas adlı bir Azure AD Yöneticisi grubu sağlar.</span><span class="sxs-lookup"><span data-stu-id="02391-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="02391-123">Komut, *ObjectID* parametresi IÇIN bir kimlik belirtir.</span><span class="sxs-lookup"><span data-stu-id="02391-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="02391-124">Bu, grubun görünen adı benzersiz olmasa bile komutun başarılı olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="02391-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="02391-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02391-125">PARAMETERS</span></span>

### <span data-ttu-id="02391-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02391-126">-DefaultProfile</span></span>
<span data-ttu-id="02391-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="02391-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02391-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="02391-128">-DisplayName</span></span>
<span data-ttu-id="02391-129">Bu cmdlet 'in sağlamasını sağlayan Azure AD yöneticisinin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02391-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02391-130">-Ismyauthentication</span><span class="sxs-lookup"><span data-stu-id="02391-130">-IsAzureADOnlyAuthentication</span></span>
<span data-ttu-id="02391-131">Yalnızca Azure Active Directory kimlik doğrulamasına izin verilip verilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="02391-131">Specifies if only Azure Active Directory authentication is allowed.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02391-132">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="02391-132">-ObjectId</span></span>
<span data-ttu-id="02391-133">Bu cmdlet 'in sağlamasını sağlayan Azure AD yöneticisinin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="02391-133">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="02391-134">Görünen ad benzersiz değilse, bu parametre için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="02391-134">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02391-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02391-135">-ResourceGroupName</span></span>
<span data-ttu-id="02391-136">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02391-136">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="02391-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="02391-137">-ServerName</span></span>
<span data-ttu-id="02391-138">Bu cmdlet 'in yönetici tarafından belirttiği SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02391-138">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02391-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="02391-139">-Confirm</span></span>
<span data-ttu-id="02391-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02391-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02391-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02391-141">-WhatIf</span></span>
<span data-ttu-id="02391-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02391-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02391-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02391-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02391-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02391-144">CommonParameters</span></span>
<span data-ttu-id="02391-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02391-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02391-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02391-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02391-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02391-147">INPUTS</span></span>

### <span data-ttu-id="02391-148">System. String</span><span class="sxs-lookup"><span data-stu-id="02391-148">System.String</span></span>

### <span data-ttu-id="02391-149">System. Guid</span><span class="sxs-lookup"><span data-stu-id="02391-149">System.Guid</span></span>

## <span data-ttu-id="02391-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02391-150">OUTPUTS</span></span>

### <span data-ttu-id="02391-151">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. model. Azureskreserveractivedirectoryadministratormodel</span><span class="sxs-lookup"><span data-stu-id="02391-151">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="02391-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02391-152">NOTES</span></span>

## <span data-ttu-id="02391-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02391-153">RELATED LINKS</span></span>

[<span data-ttu-id="02391-154">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="02391-154">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="02391-155">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="02391-155">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="02391-156">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="02391-156">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="02391-157">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="02391-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


