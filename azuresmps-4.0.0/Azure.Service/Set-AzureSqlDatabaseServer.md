---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105864"
---
# <span data-ttu-id="1ccf0-101">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1ccf0-101">Set-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="1ccf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ccf0-102">SYNOPSIS</span></span>
<span data-ttu-id="1ccf0-103">Azure SQL veritabanı sunucusunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-103">Modifies the properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="1ccf0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ccf0-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ccf0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ccf0-105">DESCRIPTION</span></span>
<span data-ttu-id="1ccf0-106">**Set-Azuressqldatabaseserver** cmdlet 'i, BELIRTILEN Azure SQL veritabanı sunucusu örneğinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-106">The **Set-AzureSqlDatabaseServer** cmdlet modifies the properties of the specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="1ccf0-107">Geçerli sürümde, yalnızca sunucunun yönetici hesabı parolasını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-107">In the current release, you can only update the administrator account password for a server.</span></span>

## <span data-ttu-id="1ccf0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ccf0-108">EXAMPLES</span></span>

### <span data-ttu-id="1ccf0-109">Örnek 1: sunucunun parolasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="1ccf0-109">Example 1: Change the password for a server</span></span>
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

<span data-ttu-id="1ccf0-110">Bu komut, lpqd0zbr8y adlı Azure SQL veritabanı sunucusu için yönetici hesabı parolasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-110">This command changes the administrator account password for the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="1ccf0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ccf0-111">PARAMETERS</span></span>

### <span data-ttu-id="1ccf0-112">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="1ccf0-112">-AdminPassword</span></span>
<span data-ttu-id="1ccf0-113">Azure SQL veritabanı sunucusu için yönetici hesabı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-113">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="1ccf0-114">Güçlü bir parola belirtmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-114">You must specify a strong password.</span></span>
<span data-ttu-id="1ccf0-115">Daha fazla bilgi [için bkz](https://go.microsoft.com/fwlink/p/?LinkId=154152) https://go.microsoft.com/fwlink/p/?LinkId=154152) .</span><span class="sxs-lookup"><span data-stu-id="1ccf0-115">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="1ccf0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1ccf0-116">-Force</span></span>
<span data-ttu-id="1ccf0-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ccf0-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="1ccf0-118">-Profile</span></span>
<span data-ttu-id="1ccf0-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ccf0-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ccf0-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1ccf0-121">-ServerName</span></span>
<span data-ttu-id="1ccf0-122">Bu cmdlet 'in değiştirdiği sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-122">Specifies the name of the server that this cmdlet modifies.</span></span>
<span data-ttu-id="1ccf0-123">Tam DNS adını değil, sunucu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-123">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccf0-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ccf0-124">-Confirm</span></span>
<span data-ttu-id="1ccf0-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ccf0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ccf0-126">-WhatIf</span></span>
<span data-ttu-id="1ccf0-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ccf0-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ccf0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ccf0-129">CommonParameters</span></span>
<span data-ttu-id="1ccf0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ccf0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ccf0-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ccf0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ccf0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ccf0-132">INPUTS</span></span>

### <span data-ttu-id="1ccf0-133">Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="1ccf0-133">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="1ccf0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ccf0-134">OUTPUTS</span></span>

## <span data-ttu-id="1ccf0-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ccf0-135">NOTES</span></span>

## <span data-ttu-id="1ccf0-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ccf0-136">RELATED LINKS</span></span>

[<span data-ttu-id="1ccf0-137">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="1ccf0-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="1ccf0-138">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="1ccf0-138">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="1ccf0-139">Get-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="1ccf0-139">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="1ccf0-140">New-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="1ccf0-140">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="1ccf0-141">Remove-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="1ccf0-141">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)


