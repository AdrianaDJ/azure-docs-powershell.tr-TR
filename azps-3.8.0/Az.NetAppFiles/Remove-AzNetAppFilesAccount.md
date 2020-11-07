---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: de0f71a91ec4445ae4be58e904e58eb3a97cb9a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937241"
---
# <span data-ttu-id="28a52-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="28a52-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="28a52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28a52-102">SYNOPSIS</span></span>
<span data-ttu-id="28a52-103">Bir Azure NetApp dosyaları (ANF) hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="28a52-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="28a52-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28a52-104">SYNTAX</span></span>

### <span data-ttu-id="28a52-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="28a52-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28a52-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="28a52-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28a52-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28a52-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28a52-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="28a52-108">DESCRIPTION</span></span>
<span data-ttu-id="28a52-109">**Remove-AzNetAppFilesAccount** cmdlet 'ı BIR ANF hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="28a52-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="28a52-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28a52-110">EXAMPLES</span></span>

### <span data-ttu-id="28a52-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="28a52-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="28a52-112">Bu komut "MyAnfAccount" ANF hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="28a52-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="28a52-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28a52-113">PARAMETERS</span></span>

### <span data-ttu-id="28a52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a52-114">-DefaultProfile</span></span>
<span data-ttu-id="28a52-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28a52-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a52-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28a52-116">-InputObject</span></span>
<span data-ttu-id="28a52-117">Kaldırılacak hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="28a52-117">The account object to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28a52-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="28a52-118">-Name</span></span>
<span data-ttu-id="28a52-119">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="28a52-119">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a52-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="28a52-120">-PassThru</span></span>
<span data-ttu-id="28a52-121">Belirtilen hesabın başarıyla kaldırıldığını döndürme</span><span class="sxs-lookup"><span data-stu-id="28a52-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="28a52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28a52-122">-ResourceGroupName</span></span>
<span data-ttu-id="28a52-123">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="28a52-123">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a52-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="28a52-124">-ResourceId</span></span>
<span data-ttu-id="28a52-125">ANF hesabının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="28a52-125">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28a52-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="28a52-126">-Confirm</span></span>
<span data-ttu-id="28a52-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="28a52-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a52-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28a52-128">-WhatIf</span></span>
<span data-ttu-id="28a52-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="28a52-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28a52-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="28a52-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a52-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a52-131">CommonParameters</span></span>
<span data-ttu-id="28a52-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28a52-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="28a52-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28a52-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a52-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28a52-134">INPUTS</span></span>

### <span data-ttu-id="28a52-135">System. String</span><span class="sxs-lookup"><span data-stu-id="28a52-135">System.String</span></span>

### <span data-ttu-id="28a52-136">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="28a52-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="28a52-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28a52-137">OUTPUTS</span></span>

### <span data-ttu-id="28a52-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28a52-138">System.Boolean</span></span>

## <span data-ttu-id="28a52-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28a52-139">NOTES</span></span>

## <span data-ttu-id="28a52-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28a52-140">RELATED LINKS</span></span>
