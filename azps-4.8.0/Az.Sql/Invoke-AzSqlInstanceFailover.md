---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266828"
---
# <span data-ttu-id="d9d78-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="d9d78-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="d9d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9d78-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d78-103">Azure SQL yönetilen örneğinin yerine çalışma.</span><span class="sxs-lookup"><span data-stu-id="d9d78-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="d9d78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9d78-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9d78-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9d78-105">DESCRIPTION</span></span>
<span data-ttu-id="d9d78-106">**Invoke-Azsqlınstancefailover** cmdlet 'ı Azure SQL yönetimli bir örneği yerine çalışma.</span><span class="sxs-lookup"><span data-stu-id="d9d78-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="d9d78-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9d78-107">EXAMPLES</span></span>

### <span data-ttu-id="d9d78-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d9d78-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="d9d78-109">Bu komut, "ManagedInstance01" adlı örneğin birincil yinelemesi yükünü devreedecektir.</span><span class="sxs-lookup"><span data-stu-id="d9d78-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="d9d78-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d9d78-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="d9d78-111">Bu komut, "ManagedInstance01" yönetilen örneğinin okunabilir ikincil çoğaltmasının yükünü devreedecektir.</span><span class="sxs-lookup"><span data-stu-id="d9d78-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="d9d78-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9d78-112">PARAMETERS</span></span>

### <span data-ttu-id="d9d78-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d9d78-113">-AsJob</span></span>
<span data-ttu-id="d9d78-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d9d78-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9d78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d78-115">-DefaultProfile</span></span>
<span data-ttu-id="d9d78-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d9d78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9d78-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d9d78-117">-Force</span></span>
<span data-ttu-id="d9d78-118">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="d9d78-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d9d78-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9d78-119">-Name</span></span>
<span data-ttu-id="d9d78-120">Kaldırılacak Azure SQL örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="d9d78-120">The name of the Azure SQL instance to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9d78-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d9d78-121">-PassThru</span></span>
<span data-ttu-id="d9d78-122">Başarılı bir yürütmede, doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="d9d78-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="d9d78-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d9d78-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d9d78-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="d9d78-124">-ReadableSecondary</span></span>
<span data-ttu-id="d9d78-125">Yük devretme varsayılan birincil çoğaltma yerine okunabilir ikincil çoğaltma</span><span class="sxs-lookup"><span data-stu-id="d9d78-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="d9d78-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d78-126">-ResourceGroupName</span></span>
<span data-ttu-id="d9d78-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d9d78-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="d9d78-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9d78-128">-Confirm</span></span>
<span data-ttu-id="d9d78-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9d78-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9d78-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9d78-130">-WhatIf</span></span>
<span data-ttu-id="d9d78-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9d78-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9d78-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9d78-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9d78-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d78-133">CommonParameters</span></span>
<span data-ttu-id="d9d78-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9d78-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d78-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d9d78-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d78-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9d78-136">INPUTS</span></span>

### <span data-ttu-id="d9d78-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d9d78-137">System.String</span></span>

## <span data-ttu-id="d9d78-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9d78-138">OUTPUTS</span></span>

## <span data-ttu-id="d9d78-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9d78-139">NOTES</span></span>

## <span data-ttu-id="d9d78-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9d78-140">RELATED LINKS</span></span>
