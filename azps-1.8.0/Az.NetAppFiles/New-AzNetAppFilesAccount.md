---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 87febe648a845d595f35c1a14b024fbd97824be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760776"
---
# <span data-ttu-id="bd4f4-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bd4f4-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="bd4f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="bd4f4-103">Yeni bir Azure NetApp dosyaları (ANF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd4f4-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="bd4f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd4f4-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd4f4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd4f4-105">DESCRIPTION</span></span>
<span data-ttu-id="bd4f4-106">**New-AzNetAppFilesAccount** cmdlet 'ı BIR ANF hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd4f4-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="bd4f4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd4f4-107">EXAMPLES</span></span>

### <span data-ttu-id="bd4f4-108">Örnek 1: ANF hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="bd4f4-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="bd4f4-109">Bu komut, "MyAnfAccount" yeni ANF hesabını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd4f4-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="bd4f4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd4f4-110">PARAMETERS</span></span>

### <span data-ttu-id="bd4f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd4f4-111">-DefaultProfile</span></span>
<span data-ttu-id="bd4f4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd4f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd4f4-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="bd4f4-113">-Location</span></span>
<span data-ttu-id="bd4f4-114">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="bd4f4-114">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd4f4-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="bd4f4-115">-Name</span></span>
<span data-ttu-id="bd4f4-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="bd4f4-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd4f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd4f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="bd4f4-118">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="bd4f4-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd4f4-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bd4f4-119">-Tag</span></span>
<span data-ttu-id="bd4f4-120">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="bd4f4-120">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd4f4-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd4f4-121">-Confirm</span></span>
<span data-ttu-id="bd4f4-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd4f4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd4f4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd4f4-123">-WhatIf</span></span>
<span data-ttu-id="bd4f4-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd4f4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd4f4-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd4f4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd4f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd4f4-126">CommonParameters</span></span>
<span data-ttu-id="bd4f4-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd4f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bd4f4-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd4f4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd4f4-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd4f4-129">INPUTS</span></span>

### <span data-ttu-id="bd4f4-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bd4f4-130">None</span></span>

## <span data-ttu-id="bd4f4-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd4f4-131">OUTPUTS</span></span>

### <span data-ttu-id="bd4f4-132">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bd4f4-132">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="bd4f4-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd4f4-133">NOTES</span></span>

## <span data-ttu-id="bd4f4-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd4f4-134">RELATED LINKS</span></span>
