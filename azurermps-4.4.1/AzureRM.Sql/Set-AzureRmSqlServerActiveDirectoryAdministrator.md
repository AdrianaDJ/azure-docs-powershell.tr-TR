---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 76d5c2fc90b4e0e518aa022a97c6b9ce369715db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591763"
---
# <span data-ttu-id="61971-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="61971-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="61971-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61971-102">SYNOPSIS</span></span>
<span data-ttu-id="61971-103">SQL Server için Azure AD yöneticisi sağlar.</span><span class="sxs-lookup"><span data-stu-id="61971-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61971-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61971-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61971-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61971-105">DESCRIPTION</span></span>
<span data-ttu-id="61971-106">**Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet 'i, geçerli abonelikteki AzureSQL Server Için bir Azure Active Directory (Azure AD) Yöneticisi sağlar.</span><span class="sxs-lookup"><span data-stu-id="61971-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

<span data-ttu-id="61971-107">Aynı anda yalnızca bir yönetici temin edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="61971-107">You can provision only one administrator at a time.</span></span>

<span data-ttu-id="61971-108">Aşağıdaki Azure AD üyeleri SQL Server Yöneticisi olarak sağlanabilir:</span><span class="sxs-lookup"><span data-stu-id="61971-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>

- <span data-ttu-id="61971-109">Yerel Azure AD üyeleri</span><span class="sxs-lookup"><span data-stu-id="61971-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="61971-110">Şirket içindeki Federasyon üyeleri</span><span class="sxs-lookup"><span data-stu-id="61971-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="61971-111">Yerel veya Federasyon üyesi olan diğer Azure reklamlardan alınan Üyeler</span><span class="sxs-lookup"><span data-stu-id="61971-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="61971-112">Güvenlik grupları olarak oluşturulan Azure AD grupları</span><span class="sxs-lookup"><span data-stu-id="61971-112">Azure AD groups created as security groups</span></span>

<span data-ttu-id="61971-113">Outlook.com, Hotmail.com veya Live.com etki alanlarında olduğu gibi Microsoft hesapları yöneticiler tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="61971-113">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="61971-114">Gmail.com veya Yahoo.com etki alanlarında olduğu gibi diğer Konuk hesapları yöneticiler tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="61971-114">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>

<span data-ttu-id="61971-115">Adanmış bir Azure AD grubunu yönetici olarak sağlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="61971-115">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="61971-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61971-116">EXAMPLES</span></span>

### <span data-ttu-id="61971-117">Örnek 1: sunucu için yönetici grubu hazırlama</span><span class="sxs-lookup"><span data-stu-id="61971-117">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="61971-118">Bu komut, server01 adlı sunucu için Vseçbas adlı bir Azure AD Yöneticisi grubu sağlar.</span><span class="sxs-lookup"><span data-stu-id="61971-118">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="61971-119">Bu sunucu, kaynak grubu ResourceGroup01 ile ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="61971-119">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="61971-120">Örnek 2: sunucu için Yönetici Kullanıcı sağlama</span><span class="sxs-lookup"><span data-stu-id="61971-120">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="61971-121">Bu komut, server01 adlı sunucunun yöneticisi olarak bir Azure AD kullanıcısı sağlar.</span><span class="sxs-lookup"><span data-stu-id="61971-121">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="61971-122">Örnek 3: KIMLIĞINI belirterek yönetici grubu hazırlama</span><span class="sxs-lookup"><span data-stu-id="61971-122">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="61971-123">Bu komut, server01 adlı sunucu için Vseçbas adlı bir Azure AD Yöneticisi grubu sağlar.</span><span class="sxs-lookup"><span data-stu-id="61971-123">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="61971-124">Komut, *ObjectID* parametresi IÇIN bir kimlik belirtir.</span><span class="sxs-lookup"><span data-stu-id="61971-124">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="61971-125">Bu, grubun görünen adı benzersiz olmasa bile komutun başarılı olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="61971-125">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="61971-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61971-126">PARAMETERS</span></span>

### <span data-ttu-id="61971-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="61971-127">-DisplayName</span></span>
<span data-ttu-id="61971-128">Bu cmdlet 'in sağlamasını sağlayan Azure AD yöneticisinin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61971-128">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="61971-129">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="61971-129">-ObjectId</span></span>
<span data-ttu-id="61971-130">Bu cmdlet 'in sağlamasını sağlayan Azure AD yöneticisinin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="61971-130">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="61971-131">Görünen ad benzersiz değilse, bu parametre için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="61971-131">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="61971-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61971-132">-ResourceGroupName</span></span>
<span data-ttu-id="61971-133">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61971-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="61971-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="61971-134">-ServerName</span></span>
<span data-ttu-id="61971-135">Bu cmdlet 'in yönetici tarafından belirttiği SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61971-135">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="61971-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="61971-136">-Confirm</span></span>
<span data-ttu-id="61971-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61971-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61971-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61971-138">-WhatIf</span></span>
<span data-ttu-id="61971-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61971-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61971-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61971-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61971-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61971-141">-DefaultProfile</span></span>
<span data-ttu-id="61971-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61971-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61971-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61971-143">CommonParameters</span></span>
<span data-ttu-id="61971-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61971-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61971-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61971-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61971-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61971-146">INPUTS</span></span>

## <span data-ttu-id="61971-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61971-147">OUTPUTS</span></span>

### <span data-ttu-id="61971-148">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. model. Azureskreserveractivedirectoryadministratormodel</span><span class="sxs-lookup"><span data-stu-id="61971-148">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="61971-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61971-149">NOTES</span></span>

## <span data-ttu-id="61971-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61971-150">RELATED LINKS</span></span>

[<span data-ttu-id="61971-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="61971-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="61971-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="61971-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="61971-153">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="61971-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


