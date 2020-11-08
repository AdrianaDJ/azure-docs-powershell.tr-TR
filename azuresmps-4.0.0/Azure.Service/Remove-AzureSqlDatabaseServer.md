---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F73A078E-F9F2-4520-BF55-DFFE82BE4466
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a8127a77ecfdc5aa36659060cb5469206a9988d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106107"
---
# <span data-ttu-id="dca45-101">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="dca45-101">Remove-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="dca45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dca45-102">SYNOPSIS</span></span>
<span data-ttu-id="dca45-103">Azure SQL veritabanı sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dca45-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="dca45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dca45-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServer -ServerName <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dca45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dca45-105">DESCRIPTION</span></span>
<span data-ttu-id="dca45-106">**Remove-Azuressqldatabaseserver** cmdlet 'i geçerli ABONELIKTEKI Azure SQL veritabanı sunucusu örneğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dca45-106">The **Remove-AzureSqlDatabaseServer** cmdlet removes the specified instance of Azure SQL Database Server from the current subscription.</span></span>
<span data-ttu-id="dca45-107">Bu cmdlet sunucudaki tüm veritabanlarını siler.</span><span class="sxs-lookup"><span data-stu-id="dca45-107">This cmdlet deletes all databases on the server.</span></span>

## <span data-ttu-id="dca45-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dca45-108">EXAMPLES</span></span>

### <span data-ttu-id="dca45-109">Örnek 1: veritabanı sunucusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="dca45-109">Example 1: Remove a database server</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="dca45-110">Bu komut, lpqd0zbr8y adlı Azure SQL veritabanı sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dca45-110">This command removes the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="dca45-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dca45-111">PARAMETERS</span></span>

### <span data-ttu-id="dca45-112">-Force</span><span class="sxs-lookup"><span data-stu-id="dca45-112">-Force</span></span>
<span data-ttu-id="dca45-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="dca45-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dca45-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="dca45-114">-Profile</span></span>
<span data-ttu-id="dca45-115">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dca45-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dca45-116">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="dca45-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dca45-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dca45-117">-ServerName</span></span>
<span data-ttu-id="dca45-118">Bu cmdlet 'in kaldırdığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dca45-118">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="dca45-119">Tam DNS adını değil, sunucu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="dca45-119">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="dca45-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="dca45-120">-Confirm</span></span>
<span data-ttu-id="dca45-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dca45-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca45-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca45-122">-WhatIf</span></span>
<span data-ttu-id="dca45-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dca45-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dca45-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dca45-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca45-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca45-125">CommonParameters</span></span>
<span data-ttu-id="dca45-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dca45-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca45-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca45-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca45-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dca45-128">INPUTS</span></span>

### <span data-ttu-id="dca45-129">Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="dca45-129">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="dca45-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dca45-130">OUTPUTS</span></span>

## <span data-ttu-id="dca45-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dca45-131">NOTES</span></span>

## <span data-ttu-id="dca45-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dca45-132">RELATED LINKS</span></span>

[<span data-ttu-id="dca45-133">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="dca45-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="dca45-134">Sunucu silme</span><span class="sxs-lookup"><span data-stu-id="dca45-134">Delete Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505695.aspx)

[<span data-ttu-id="dca45-135">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="dca45-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="dca45-136">Get-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="dca45-136">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="dca45-137">New-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="dca45-137">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="dca45-138">Set-Azuressqldatabaseserver</span><span class="sxs-lookup"><span data-stu-id="dca45-138">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


