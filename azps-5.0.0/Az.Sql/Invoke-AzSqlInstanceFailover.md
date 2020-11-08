---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275656"
---
# <span data-ttu-id="7431e-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="7431e-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="7431e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7431e-102">SYNOPSIS</span></span>
<span data-ttu-id="7431e-103">Azure SQL yönetilen örneğinin yerine çalışma.</span><span class="sxs-lookup"><span data-stu-id="7431e-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="7431e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7431e-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7431e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7431e-105">DESCRIPTION</span></span>
<span data-ttu-id="7431e-106">**Invoke-Azsqlınstancefailover** cmdlet 'ı Azure SQL yönetimli bir örneği yerine çalışma.</span><span class="sxs-lookup"><span data-stu-id="7431e-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="7431e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7431e-107">EXAMPLES</span></span>

### <span data-ttu-id="7431e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7431e-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="7431e-109">Bu komut, "ManagedInstance01" adlı örneğin birincil yinelemesi yükünü devreedecektir.</span><span class="sxs-lookup"><span data-stu-id="7431e-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="7431e-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7431e-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="7431e-111">Bu komut, "ManagedInstance01" yönetilen örneğinin okunabilir ikincil çoğaltmasının yükünü devreedecektir.</span><span class="sxs-lookup"><span data-stu-id="7431e-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="7431e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7431e-112">PARAMETERS</span></span>

### <span data-ttu-id="7431e-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="7431e-113">-AsJob</span></span>
<span data-ttu-id="7431e-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7431e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7431e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7431e-115">-DefaultProfile</span></span>
<span data-ttu-id="7431e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7431e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7431e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7431e-117">-Force</span></span>
<span data-ttu-id="7431e-118">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="7431e-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7431e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7431e-119">-Name</span></span>
<span data-ttu-id="7431e-120">Kaldırılacak Azure SQL örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="7431e-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="7431e-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7431e-121">-PassThru</span></span>
<span data-ttu-id="7431e-122">Başarılı bir yürütmede, doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="7431e-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="7431e-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7431e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7431e-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="7431e-124">-ReadableSecondary</span></span>
<span data-ttu-id="7431e-125">Yük devretme varsayılan birincil çoğaltma yerine okunabilir ikincil çoğaltma</span><span class="sxs-lookup"><span data-stu-id="7431e-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="7431e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7431e-126">-ResourceGroupName</span></span>
<span data-ttu-id="7431e-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7431e-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="7431e-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="7431e-128">-Confirm</span></span>
<span data-ttu-id="7431e-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7431e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7431e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7431e-130">-WhatIf</span></span>
<span data-ttu-id="7431e-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7431e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7431e-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7431e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7431e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7431e-133">CommonParameters</span></span>
<span data-ttu-id="7431e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7431e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7431e-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7431e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7431e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7431e-136">INPUTS</span></span>

### <span data-ttu-id="7431e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7431e-137">System.String</span></span>

## <span data-ttu-id="7431e-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7431e-138">OUTPUTS</span></span>

## <span data-ttu-id="7431e-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7431e-139">NOTES</span></span>

## <span data-ttu-id="7431e-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7431e-140">RELATED LINKS</span></span>
