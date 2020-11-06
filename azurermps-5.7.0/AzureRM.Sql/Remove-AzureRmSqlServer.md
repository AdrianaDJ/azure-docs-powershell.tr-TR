---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 76b4e024f5a6d5979bbcd9aa860caee823ecc28e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589663"
---
# <span data-ttu-id="1988c-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="1988c-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="1988c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1988c-102">SYNOPSIS</span></span>
<span data-ttu-id="1988c-103">Azure SQL veritabanı sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1988c-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1988c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1988c-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1988c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1988c-105">DESCRIPTION</span></span>
<span data-ttu-id="1988c-106">**Remove-AzureRmSqlServer** cmdlet 'ı BIR Azure SQL veritabanı sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1988c-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="1988c-107">Silme işlemi zaman uyumsuzdur ve biraz zaman alabilir, bu nedenle tamamen silinen sunucuya bağlı olan ek işlemleri gerçekleştirmeden önce işlemin bitiryapıldığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="1988c-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="1988c-108">Örneğin, aynı adı kullanan yeni bir sunucu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1988c-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="1988c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1988c-109">EXAMPLES</span></span>

### <span data-ttu-id="1988c-110">Örnek 1: sunucu kaldırma</span><span class="sxs-lookup"><span data-stu-id="1988c-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="1988c-111">Bu komut, server01 adlı Azure SQL veritabanı sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1988c-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="1988c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1988c-112">PARAMETERS</span></span>

### <span data-ttu-id="1988c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1988c-113">-DefaultProfile</span></span>
<span data-ttu-id="1988c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1988c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1988c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1988c-115">-Force</span></span>
<span data-ttu-id="1988c-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="1988c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1988c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1988c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1988c-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1988c-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1988c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1988c-119">-ServerName</span></span>
<span data-ttu-id="1988c-120">Kaldırılacak sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1988c-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1988c-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="1988c-121">-Confirm</span></span>
<span data-ttu-id="1988c-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1988c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1988c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1988c-123">-WhatIf</span></span>
<span data-ttu-id="1988c-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1988c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1988c-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1988c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1988c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1988c-126">CommonParameters</span></span>
<span data-ttu-id="1988c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1988c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1988c-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1988c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1988c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1988c-129">INPUTS</span></span>

### <span data-ttu-id="1988c-130">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="1988c-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="1988c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1988c-131">OUTPUTS</span></span>

### <span data-ttu-id="1988c-132">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="1988c-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="1988c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1988c-133">NOTES</span></span>

## <span data-ttu-id="1988c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1988c-134">RELATED LINKS</span></span>

[<span data-ttu-id="1988c-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="1988c-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="1988c-136">Yeni-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="1988c-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="1988c-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="1988c-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="1988c-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="1988c-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


