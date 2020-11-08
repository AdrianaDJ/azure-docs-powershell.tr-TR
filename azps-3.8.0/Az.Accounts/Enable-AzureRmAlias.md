---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 63873d3eb1c46b5c2a4004e9c361f87e74e73eba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098501"
---
# <span data-ttu-id="bc050-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="bc050-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="bc050-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc050-102">SYNOPSIS</span></span>
<span data-ttu-id="bc050-103">Az modüllerle AzureRm önek diğer adlarını verir.</span><span class="sxs-lookup"><span data-stu-id="bc050-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="bc050-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc050-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc050-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc050-105">DESCRIPTION</span></span>
<span data-ttu-id="bc050-106">Az modüllerle AzureRm önek diğer adlarını verir.</span><span class="sxs-lookup"><span data-stu-id="bc050-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="bc050-107">-Module belirtilirse, yalnızca listelenen modüllerin diğer adları etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bc050-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="bc050-108">Aksi takdirde tüm AzureRm diğer adları etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bc050-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="bc050-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc050-109">EXAMPLES</span></span>

### <span data-ttu-id="bc050-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc050-110">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="bc050-111">Geçerli PowerShell oturumunun tüm AzureRm öneklerini etkin kılar.</span><span class="sxs-lookup"><span data-stu-id="bc050-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="bc050-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc050-112">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="bc050-113">Hem geçerli süreç hem de geçerli kullanıcı için en az. hesaplar modülü için AzureRm diğer adlarını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="bc050-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="bc050-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc050-114">PARAMETERS</span></span>

### <span data-ttu-id="bc050-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc050-115">-DefaultProfile</span></span>
<span data-ttu-id="bc050-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc050-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc050-117">-Modül</span><span class="sxs-lookup"><span data-stu-id="bc050-117">-Module</span></span>
<span data-ttu-id="bc050-118">Diğer adların hangi modülleri etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc050-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="bc050-119">Hiçbiri belirtilmemişse, varsayılan tüm modüller olur.</span><span class="sxs-lookup"><span data-stu-id="bc050-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="bc050-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bc050-120">-PassThru</span></span>
<span data-ttu-id="bc050-121">Belirtilmişse cmdlet 'in etkinleştirildiği tüm diğer adlar</span><span class="sxs-lookup"><span data-stu-id="bc050-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="bc050-122">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="bc050-122">-Scope</span></span>
<span data-ttu-id="bc050-123">Hangi kapsam diğer adlarının etkinleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc050-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="bc050-124">Varsayılan: ' yerel '</span><span class="sxs-lookup"><span data-stu-id="bc050-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="bc050-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc050-125">-Confirm</span></span>
<span data-ttu-id="bc050-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc050-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc050-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc050-127">-WhatIf</span></span>
<span data-ttu-id="bc050-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc050-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc050-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc050-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc050-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc050-130">CommonParameters</span></span>
<span data-ttu-id="bc050-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc050-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc050-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc050-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc050-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc050-133">INPUTS</span></span>

### <span data-ttu-id="bc050-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bc050-134">None</span></span>

## <span data-ttu-id="bc050-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc050-135">OUTPUTS</span></span>

### <span data-ttu-id="bc050-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bc050-136">System.String</span></span>

## <span data-ttu-id="bc050-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc050-137">NOTES</span></span>

## <span data-ttu-id="bc050-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc050-138">RELATED LINKS</span></span>
