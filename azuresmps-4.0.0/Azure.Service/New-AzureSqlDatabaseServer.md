---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A0C674FC-A1D8-4068-8CAB-2EE0AECB8E68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 069b96809c0659028135e8c9a28e7e3c0ab8b3ae
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105971"
---
# <span data-ttu-id="c5887-101">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c5887-101">New-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="c5887-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5887-102">SYNOPSIS</span></span>
<span data-ttu-id="c5887-103">Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c5887-103">Creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="c5887-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5887-104">SYNTAX</span></span>

```
New-AzureSqlDatabaseServer -AdministratorLogin <String> -AdministratorLoginPassword <String> -Location <String>
 [-Version <Single>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5887-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5887-105">DESCRIPTION</span></span>
<span data-ttu-id="c5887-106">**New-Azuressqldatabaseserver** cmdlet 'i geçerli ABONELIKTE Azure SQL veritabanı sunucusu örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c5887-106">The **New-AzureSqlDatabaseServer** cmdlet creates an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="c5887-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5887-107">EXAMPLES</span></span>

### <span data-ttu-id="c5887-108">Örnek 1: sunucu oluşturma</span><span class="sxs-lookup"><span data-stu-id="c5887-108">Example 1: Create a server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword"
```

<span data-ttu-id="c5887-109">Bu komut, bir sürüm 11 Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c5887-109">This command creates a version 11 Azure SQL Database server.</span></span>

### <span data-ttu-id="c5887-110">Örnek 2: sürüm 12 sunucusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="c5887-110">Example 2: Create a version 12 server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword" -Version "12.0"
```

<span data-ttu-id="c5887-111">Bu komut 12 sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c5887-111">This command creates a version 12 server.</span></span>

## <span data-ttu-id="c5887-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5887-112">PARAMETERS</span></span>

### <span data-ttu-id="c5887-113">-\Administrators oturum açma</span><span class="sxs-lookup"><span data-stu-id="c5887-113">-AdministratorLogin</span></span>
<span data-ttu-id="c5887-114">Yeni Azure SQL veritabanı sunucusu için yönetici hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5887-114">Specifies the administrator account name for the new Azure SQL Database server.</span></span>

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

### <span data-ttu-id="c5887-115">-\Administrators</span><span class="sxs-lookup"><span data-stu-id="c5887-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="c5887-116">Azure SQL veritabanı sunucusu için yönetici hesabı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5887-116">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="c5887-117">Güçlü bir parola belirtmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="c5887-117">You must specify a strong password.</span></span>
<span data-ttu-id="c5887-118">Daha fazla bilgi [için bkz](https://go.microsoft.com/fwlink/p/?LinkId=154152) https://go.microsoft.com/fwlink/p/?LinkId=154152) .</span><span class="sxs-lookup"><span data-stu-id="c5887-118">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="c5887-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c5887-119">-Force</span></span>
<span data-ttu-id="c5887-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c5887-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5887-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="c5887-121">-Location</span></span>
<span data-ttu-id="c5887-122">Bu cmdlet 'in sunucuyu oluşturduğu veri merkezinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5887-122">Specifies the location of the data center where this cmdlet creates the server.</span></span>
<span data-ttu-id="c5887-123">Daha fazla bilgi için bkz: [Azure](https://azure.microsoft.com/regions/) https://azure.microsoft.com/regions/#services) Library.</span><span class="sxs-lookup"><span data-stu-id="c5887-123">For more information, see [Azure Regions](https://azure.microsoft.com/regions/) (https://azure.microsoft.com/regions/#services) in the Azure library.</span></span>

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

### <span data-ttu-id="c5887-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="c5887-124">-Profile</span></span>
<span data-ttu-id="c5887-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5887-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5887-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c5887-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5887-127">-Version</span><span class="sxs-lookup"><span data-stu-id="c5887-127">-Version</span></span>
<span data-ttu-id="c5887-128">Yeni sunucunun sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5887-128">Specifies the version of the new server.</span></span>
<span data-ttu-id="c5887-129">Geçerli değerler: 2,0 ve 12,0.</span><span class="sxs-lookup"><span data-stu-id="c5887-129">Valid values are: 2.0 and 12.0.</span></span>

```yaml
Type: Single
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5887-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c5887-130">-Confirm</span></span>
<span data-ttu-id="c5887-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c5887-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5887-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5887-132">-WhatIf</span></span>
<span data-ttu-id="c5887-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5887-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5887-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c5887-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5887-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5887-135">CommonParameters</span></span>
<span data-ttu-id="c5887-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5887-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5887-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5887-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5887-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5887-138">INPUTS</span></span>

## <span data-ttu-id="c5887-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5887-139">OUTPUTS</span></span>

### <span data-ttu-id="c5887-140">Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="c5887-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="c5887-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5887-141">NOTES</span></span>

## <span data-ttu-id="c5887-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5887-142">RELATED LINKS</span></span>

[<span data-ttu-id="c5887-143">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="c5887-143">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c5887-144">Sunucu oluşturma</span><span class="sxs-lookup"><span data-stu-id="c5887-144">Create Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505699.aspx)

[<span data-ttu-id="c5887-145">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="c5887-145">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c5887-146">Get-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="c5887-146">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="c5887-147">Remove-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="c5887-147">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="c5887-148">Set-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="c5887-148">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


