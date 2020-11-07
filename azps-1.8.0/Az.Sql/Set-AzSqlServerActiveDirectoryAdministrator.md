---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 44339cb39396b18660d17bdbad0e597ded30ad18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758760"
---
# <span data-ttu-id="8252a-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8252a-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="8252a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8252a-102">SYNOPSIS</span></span>
<span data-ttu-id="8252a-103">SQL Server için Azure AD yöneticisi sağlar.</span><span class="sxs-lookup"><span data-stu-id="8252a-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="8252a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8252a-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8252a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8252a-105">DESCRIPTION</span></span>
<span data-ttu-id="8252a-106">**Set-AzSqlServerActiveDirectoryAdministrator** cmdlet 'i, geçerli abonelikteki AzureSQL Server Için Azure Active Directory (Azure AD) Yöneticisi sağlar.</span><span class="sxs-lookup"><span data-stu-id="8252a-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="8252a-107">Aynı anda yalnızca bir yönetici temin edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8252a-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="8252a-108">Aşağıdaki Azure AD üyeleri SQL Server Yöneticisi olarak sağlanabilir:</span><span class="sxs-lookup"><span data-stu-id="8252a-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="8252a-109">Yerel Azure AD üyeleri</span><span class="sxs-lookup"><span data-stu-id="8252a-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="8252a-110">Şirket içindeki Federasyon üyeleri</span><span class="sxs-lookup"><span data-stu-id="8252a-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="8252a-111">Yerel veya Federasyon üyesi olan diğer Azure reklamlardan alınan Üyeler</span><span class="sxs-lookup"><span data-stu-id="8252a-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="8252a-112">Güvenlik grupları olarak oluşturulan Azure AD grupları, Outlook.com, Hotmail.com veya Live.com etki alanlarında olduğu gibi, yöneticiler tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="8252a-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="8252a-113">Gmail.com veya Yahoo.com etki alanlarında olduğu gibi diğer Konuk hesapları yöneticiler tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="8252a-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="8252a-114">Adanmış bir Azure AD grubunu yönetici olarak sağlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="8252a-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="8252a-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8252a-115">EXAMPLES</span></span>

### <span data-ttu-id="8252a-116">Örnek 1: sunucu için yönetici grubu hazırlama</span><span class="sxs-lookup"><span data-stu-id="8252a-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="8252a-117">Bu komut, server01 adlı sunucu için Vseçbas adlı bir Azure AD Yöneticisi grubu sağlar.</span><span class="sxs-lookup"><span data-stu-id="8252a-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="8252a-118">Bu sunucu, kaynak grubu ResourceGroup01 ile ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8252a-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="8252a-119">Örnek 2: sunucu için Yönetici Kullanıcı sağlama</span><span class="sxs-lookup"><span data-stu-id="8252a-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="8252a-120">Bu komut, server01 adlı sunucunun yöneticisi olarak bir Azure AD kullanıcısı sağlar.</span><span class="sxs-lookup"><span data-stu-id="8252a-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="8252a-121">Örnek 3: KIMLIĞINI belirterek yönetici grubu hazırlama</span><span class="sxs-lookup"><span data-stu-id="8252a-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="8252a-122">Bu komut, server01 adlı sunucu için Vseçbas adlı bir Azure AD Yöneticisi grubu sağlar.</span><span class="sxs-lookup"><span data-stu-id="8252a-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="8252a-123">Komut, *ObjectID* parametresi IÇIN bir kimlik belirtir.</span><span class="sxs-lookup"><span data-stu-id="8252a-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="8252a-124">Bu, grubun görünen adı benzersiz olmasa bile komutun başarılı olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="8252a-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="8252a-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8252a-125">PARAMETERS</span></span>

### <span data-ttu-id="8252a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8252a-126">-DefaultProfile</span></span>
<span data-ttu-id="8252a-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8252a-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8252a-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8252a-128">-DisplayName</span></span>
<span data-ttu-id="8252a-129">Bu cmdlet 'in sağlamasını sağlayan Azure AD yöneticisinin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8252a-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="8252a-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="8252a-130">-ObjectId</span></span>
<span data-ttu-id="8252a-131">Bu cmdlet 'in sağlamasını sağlayan Azure AD yöneticisinin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8252a-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="8252a-132">Görünen ad benzersiz değilse, bu parametre için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8252a-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="8252a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8252a-133">-ResourceGroupName</span></span>
<span data-ttu-id="8252a-134">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8252a-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8252a-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8252a-135">-ServerName</span></span>
<span data-ttu-id="8252a-136">Bu cmdlet 'in yönetici tarafından belirttiği SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8252a-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="8252a-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="8252a-137">-Confirm</span></span>
<span data-ttu-id="8252a-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8252a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8252a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8252a-139">-WhatIf</span></span>
<span data-ttu-id="8252a-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8252a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8252a-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8252a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8252a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8252a-142">CommonParameters</span></span>
<span data-ttu-id="8252a-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8252a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8252a-144">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8252a-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8252a-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8252a-145">INPUTS</span></span>

### <span data-ttu-id="8252a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8252a-146">System.String</span></span>

### <span data-ttu-id="8252a-147">System. Guid</span><span class="sxs-lookup"><span data-stu-id="8252a-147">System.Guid</span></span>

## <span data-ttu-id="8252a-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8252a-148">OUTPUTS</span></span>

### <span data-ttu-id="8252a-149">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. model. Azureskreserveractivedirectoryadministratormodel</span><span class="sxs-lookup"><span data-stu-id="8252a-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="8252a-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8252a-150">NOTES</span></span>

## <span data-ttu-id="8252a-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8252a-151">RELATED LINKS</span></span>

[<span data-ttu-id="8252a-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8252a-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="8252a-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8252a-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="8252a-154">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="8252a-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


