---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 24862931e19d0e8b8c7b8568aabb6f25cf65f9c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751282"
---
# <span data-ttu-id="ba355-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ba355-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="ba355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba355-102">SYNOPSIS</span></span>
<span data-ttu-id="ba355-103">Az modüllerle AzureRm önek diğer adlarını verir.</span><span class="sxs-lookup"><span data-stu-id="ba355-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="ba355-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba355-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba355-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba355-105">DESCRIPTION</span></span>
<span data-ttu-id="ba355-106">Az modüllerle AzureRm önek diğer adlarını verir.</span><span class="sxs-lookup"><span data-stu-id="ba355-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="ba355-107">-Module belirtilirse, yalnızca listelenen modüllerin diğer adları etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ba355-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="ba355-108">Aksi takdirde tüm AzureRm diğer adları etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ba355-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="ba355-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba355-109">EXAMPLES</span></span>

### <span data-ttu-id="ba355-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ba355-110">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="ba355-111">Geçerli PowerShell oturumunun tüm AzureRm öneklerini etkin kılar.</span><span class="sxs-lookup"><span data-stu-id="ba355-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="ba355-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ba355-112">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="ba355-113">Hem geçerli süreç hem de geçerli kullanıcı için en az. hesaplar modülü için AzureRm diğer adlarını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="ba355-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="ba355-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba355-114">PARAMETERS</span></span>

### <span data-ttu-id="ba355-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba355-115">-DefaultProfile</span></span>
<span data-ttu-id="ba355-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba355-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba355-117">-Modül</span><span class="sxs-lookup"><span data-stu-id="ba355-117">-Module</span></span>
<span data-ttu-id="ba355-118">Diğer adların hangi modülleri etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba355-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="ba355-119">Hiçbiri belirtilmemişse, varsayılan tüm modüller olur.</span><span class="sxs-lookup"><span data-stu-id="ba355-119">If none are specified, default is all modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba355-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ba355-120">-PassThru</span></span>
<span data-ttu-id="ba355-121">Belirtilmişse cmdlet 'in etkinleştirildiği tüm diğer adlar</span><span class="sxs-lookup"><span data-stu-id="ba355-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="ba355-122">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="ba355-122">-Scope</span></span>
<span data-ttu-id="ba355-123">Hangi kapsam diğer adlarının etkinleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba355-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="ba355-124">Varsayılan: ' yerel '</span><span class="sxs-lookup"><span data-stu-id="ba355-124">Default is 'Local'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba355-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba355-125">-Confirm</span></span>
<span data-ttu-id="ba355-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba355-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba355-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba355-127">-WhatIf</span></span>
<span data-ttu-id="ba355-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba355-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba355-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba355-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba355-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba355-130">CommonParameters</span></span>
<span data-ttu-id="ba355-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba355-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba355-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba355-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba355-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba355-133">INPUTS</span></span>

### <span data-ttu-id="ba355-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ba355-134">None</span></span>

## <span data-ttu-id="ba355-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba355-135">OUTPUTS</span></span>

### <span data-ttu-id="ba355-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ba355-136">System.String</span></span>

## <span data-ttu-id="ba355-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba355-137">NOTES</span></span>

## <span data-ttu-id="ba355-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba355-138">RELATED LINKS</span></span>
