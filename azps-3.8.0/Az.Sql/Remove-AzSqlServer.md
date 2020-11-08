---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 670b3e6ec71a768fe40bbcf542440db5ec685b2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098419"
---
# <span data-ttu-id="7f117-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="7f117-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="7f117-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f117-102">SYNOPSIS</span></span>
<span data-ttu-id="7f117-103">Azure SQL veritabanı sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7f117-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="7f117-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f117-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f117-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f117-105">DESCRIPTION</span></span>
<span data-ttu-id="7f117-106">**Remove-AzSqlServer** cmdlet 'ı BIR Azure SQL veritabanı sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7f117-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="7f117-107">Silme işlemi zaman uyumsuzdur ve biraz zaman alabilir, bu nedenle tamamen silinen sunucuya bağlı olan ek işlemleri gerçekleştirmeden önce işlemin bitiryapıldığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="7f117-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="7f117-108">Örneğin, aynı adı kullanan yeni bir sunucu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7f117-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="7f117-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f117-109">EXAMPLES</span></span>

### <span data-ttu-id="7f117-110">Örnek 1: sunucu kaldırma</span><span class="sxs-lookup"><span data-stu-id="7f117-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="7f117-111">Bu komut, server01 adlı Azure SQL veritabanı sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7f117-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="7f117-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f117-112">PARAMETERS</span></span>

### <span data-ttu-id="7f117-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f117-113">-DefaultProfile</span></span>
<span data-ttu-id="7f117-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7f117-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f117-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7f117-115">-Force</span></span>
<span data-ttu-id="7f117-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7f117-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f117-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f117-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f117-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f117-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7f117-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7f117-119">-ServerName</span></span>
<span data-ttu-id="7f117-120">Kaldırılacak sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f117-120">Specifies the name of the server to remove.</span></span>

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

### <span data-ttu-id="7f117-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f117-121">-Confirm</span></span>
<span data-ttu-id="7f117-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f117-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f117-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f117-123">-WhatIf</span></span>
<span data-ttu-id="7f117-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f117-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f117-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f117-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f117-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f117-126">CommonParameters</span></span>
<span data-ttu-id="7f117-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f117-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f117-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7f117-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f117-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f117-129">INPUTS</span></span>

### <span data-ttu-id="7f117-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7f117-130">System.String</span></span>

## <span data-ttu-id="7f117-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f117-131">OUTPUTS</span></span>

### <span data-ttu-id="7f117-132">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="7f117-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="7f117-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f117-133">NOTES</span></span>

## <span data-ttu-id="7f117-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f117-134">RELATED LINKS</span></span>

[<span data-ttu-id="7f117-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="7f117-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="7f117-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="7f117-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="7f117-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="7f117-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="7f117-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="7f117-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

