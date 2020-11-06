---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: e6a47578ef2442e6ca2f6d03284624f1f2906e35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588238"
---
# <span data-ttu-id="dbf9e-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dbf9e-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="dbf9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbf9e-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf9e-103">Tehdit algılama ilkesini sunucudan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbf9e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbf9e-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf9e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbf9e-105">DESCRIPTION</span></span>
<span data-ttu-id="dbf9e-106">Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet 'i Azure SQL Server 'dan tehdit algılama ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="dbf9e-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ilkeyi kaldırdığı sunucuyu belirlemek için ResourceGroupName ve ServerName parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="dbf9e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbf9e-108">EXAMPLES</span></span>

### <span data-ttu-id="dbf9e-109">--------------------------Örnek 1: veritabanı için tehdit algılama ilkesini kaldırma--------------------------</span><span class="sxs-lookup"><span data-stu-id="dbf9e-109">--------------------------  Example 1: Remove a threat detection policy for a database  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="dbf9e-110">Bu komut, tehdit algılama ilkesini server01 adlı sunucudan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="dbf9e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbf9e-111">PARAMETERS</span></span>

### <span data-ttu-id="dbf9e-112">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dbf9e-112">-PassThru</span></span>
<span data-ttu-id="dbf9e-113">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dbf9e-114">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dbf9e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf9e-115">-ResourceGroupName</span></span>
<span data-ttu-id="dbf9e-116">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-116">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="dbf9e-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dbf9e-117">-ServerName</span></span>
<span data-ttu-id="dbf9e-118">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-118">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbf9e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="dbf9e-119">-Confirm</span></span>
<span data-ttu-id="dbf9e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf9e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf9e-121">-WhatIf</span></span>
<span data-ttu-id="dbf9e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbf9e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf9e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf9e-124">-DefaultProfile</span></span>
<span data-ttu-id="dbf9e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbf9e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf9e-126">CommonParameters</span></span>
<span data-ttu-id="dbf9e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf9e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbf9e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf9e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbf9e-129">INPUTS</span></span>

###  
<span data-ttu-id="dbf9e-130">Bu cmdlet 'e giriş kanalı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="dbf9e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbf9e-131">OUTPUTS</span></span>

### <span data-ttu-id="dbf9e-132">Microsoft. Azure. Commands. Sql. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="dbf9e-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="dbf9e-133">Bu cmdlet bir ServerThreatDetectionPolicyModel nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="dbf9e-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="dbf9e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbf9e-134">NOTES</span></span>

## <span data-ttu-id="dbf9e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbf9e-135">RELATED LINKS</span></span>

[<span data-ttu-id="dbf9e-136">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="dbf9e-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

