---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f59796a51ccd1f3e5e77442cde434ab803d0781
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932131"
---
# <span data-ttu-id="c609f-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c609f-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="c609f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c609f-102">SYNOPSIS</span></span>
<span data-ttu-id="c609f-103">Bir Azure NetApp dosyaları (ANF) hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="c609f-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="c609f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c609f-104">SYNTAX</span></span>

### <span data-ttu-id="c609f-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c609f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c609f-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c609f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c609f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c609f-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c609f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c609f-108">DESCRIPTION</span></span>
<span data-ttu-id="c609f-109">**Remove-AzNetAppFilesAccount** cmdlet 'ı BIR ANF hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="c609f-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="c609f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c609f-110">EXAMPLES</span></span>

### <span data-ttu-id="c609f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c609f-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="c609f-112">Bu komut "MyAnfAccount" ANF hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="c609f-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="c609f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c609f-113">PARAMETERS</span></span>

### <span data-ttu-id="c609f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c609f-114">-DefaultProfile</span></span>
<span data-ttu-id="c609f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c609f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c609f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c609f-116">-InputObject</span></span>
<span data-ttu-id="c609f-117">Kaldırılacak hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="c609f-117">The account object to remove</span></span>

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

### <span data-ttu-id="c609f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c609f-118">-Name</span></span>
<span data-ttu-id="c609f-119">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="c609f-119">The name of the ANF account</span></span>

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

### <span data-ttu-id="c609f-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c609f-120">-PassThru</span></span>
<span data-ttu-id="c609f-121">Belirtilen hesabın başarıyla kaldırıldığını döndürme</span><span class="sxs-lookup"><span data-stu-id="c609f-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="c609f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c609f-122">-ResourceGroupName</span></span>
<span data-ttu-id="c609f-123">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="c609f-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c609f-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c609f-124">-ResourceId</span></span>
<span data-ttu-id="c609f-125">ANF hesabının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c609f-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="c609f-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="c609f-126">-Confirm</span></span>
<span data-ttu-id="c609f-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c609f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c609f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c609f-128">-WhatIf</span></span>
<span data-ttu-id="c609f-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c609f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c609f-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c609f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c609f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c609f-131">CommonParameters</span></span>
<span data-ttu-id="c609f-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c609f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c609f-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c609f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c609f-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c609f-134">INPUTS</span></span>

### <span data-ttu-id="c609f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c609f-135">System.String</span></span>

### <span data-ttu-id="c609f-136">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c609f-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="c609f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c609f-137">OUTPUTS</span></span>

### <span data-ttu-id="c609f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c609f-138">System.Boolean</span></span>

## <span data-ttu-id="c609f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c609f-139">NOTES</span></span>

## <span data-ttu-id="c609f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c609f-140">RELATED LINKS</span></span>
