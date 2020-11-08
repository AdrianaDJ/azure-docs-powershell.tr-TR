---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f6e2421a20cb7aaf044d3abfbbddf7f5c72b37e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275715"
---
# <span data-ttu-id="49ca8-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="49ca8-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="49ca8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="49ca8-103">Bir Azure NetApp dosyaları (ANF) hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="49ca8-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="49ca8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49ca8-104">SYNTAX</span></span>

### <span data-ttu-id="49ca8-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="49ca8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ca8-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="49ca8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ca8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ca8-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ca8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="49ca8-108">DESCRIPTION</span></span>
<span data-ttu-id="49ca8-109">**Remove-AzNetAppFilesAccount** cmdlet 'ı BIR ANF hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="49ca8-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="49ca8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49ca8-110">EXAMPLES</span></span>

### <span data-ttu-id="49ca8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="49ca8-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="49ca8-112">Bu komut "MyAnfAccount" ANF hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="49ca8-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="49ca8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49ca8-113">PARAMETERS</span></span>

### <span data-ttu-id="49ca8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ca8-114">-DefaultProfile</span></span>
<span data-ttu-id="49ca8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49ca8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49ca8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49ca8-116">-InputObject</span></span>
<span data-ttu-id="49ca8-117">Kaldırılacak hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="49ca8-117">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="49ca8-118">-Name</span></span>
<span data-ttu-id="49ca8-119">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="49ca8-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="49ca8-120">-PassThru</span></span>
<span data-ttu-id="49ca8-121">Belirtilen hesabın başarıyla kaldırıldığını döndürme</span><span class="sxs-lookup"><span data-stu-id="49ca8-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="49ca8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49ca8-122">-ResourceGroupName</span></span>
<span data-ttu-id="49ca8-123">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="49ca8-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="49ca8-124">-ResourceId</span></span>
<span data-ttu-id="49ca8-125">ANF hesabının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="49ca8-125">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="49ca8-126">-Confirm</span></span>
<span data-ttu-id="49ca8-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="49ca8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49ca8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ca8-128">-WhatIf</span></span>
<span data-ttu-id="49ca8-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="49ca8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49ca8-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="49ca8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49ca8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ca8-131">CommonParameters</span></span>
<span data-ttu-id="49ca8-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49ca8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ca8-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="49ca8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ca8-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49ca8-134">INPUTS</span></span>

### <span data-ttu-id="49ca8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="49ca8-135">System.String</span></span>

### <span data-ttu-id="49ca8-136">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="49ca8-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="49ca8-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49ca8-137">OUTPUTS</span></span>

### <span data-ttu-id="49ca8-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49ca8-138">System.Boolean</span></span>

## <span data-ttu-id="49ca8-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49ca8-139">NOTES</span></span>

## <span data-ttu-id="49ca8-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49ca8-140">RELATED LINKS</span></span>
